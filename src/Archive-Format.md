# Archive format

From client revision 194 until 377, all the files in cache 0
are in an archive-like format which contains a collection of named
files (e.g. `BADENC.TXT` is a file which contains bad words in the
`wordenc` archive).

## Usage

These files are used by the client for a variety of purpose.

The files themselves represent either an index, which contains
information about to where to locate data in the cache, and
the data themselves.

e.g. `DATA` contains data for interfaces.

e.g. `MAP_INDEX` contains information about where to find the map and landscape files in the cache.

## Format

```
tribyte uncompressedSize
tribyte compressedSize
```

If the uncompressed and compressed sizes are equal, the whole file is
not compressed but the individual entries are compressed using bzip2.
If they are not equal, the entire file is compressed using bzip2 but
the individual entries are not.

Note: The magic id at the start of the bzip2 entries are not included
in the cache.
If you use an existing API to read the files and want to add this back,
you must append the characters `BZh1` before you decompress.

```short fileCount```

Each file entry has the format:

```
int nameHash
tribyte uncompressedSize
tribyte compressedSize
```

# Extracting the data

If you iterate over the files using a for-loop, you need to keep track of the
file offset.
The following pseudo-code demonstates how:

```java
int offset = buffer.getCurrentOffset() + numFiles * 10;

for(int i = 0; i < numFiles; i++) {
    // read values
    int thisFileOffset = offset;
    offset += thisFileCompressedSize;
}
```

To acquire a named file using its name, hash the name as follows:

```java
public static int hash(String name) {
    int hash = 0;
    name = name.toUpperCase();
    
    for(int j = 0; j < name.length(); j++) {
        hash = (hash * 61 + name.charAt(j)) - 32;
    }
    return hash;
}
```

Then, loop through the file entries you loaded earlier to find a
matching hash. Read the compressed file size from the offset. If the
whole file is not compressed, you should decompress the individual
entry.

## \#194 Archive Format

The \#194 (RuneScape 2 beta) client worked with a very simple cache
format.
Each file in the cache corresponded to a file on the operating system.

### Name hashing

Every name in the cache was hashed using the following method which is,
incidentally, similar to the way player names are converted to longs.

```java
public static final long gethash(String string) {
    string = string.trim();
    long l = 0L;
    
    for (int i = 0; i < string.length() && i < 12; i++) {
        char c = string.charAt(i);
        l \*= 37L;
        
        if (c >= 'A' && c <= 'Z')
            l += (long) ('\\001' + c - 'A');
        else if (c >= 'a' && c <= 'z')
            l += (long) ('\\001' + c - 'a');
        else if (c >= '0' && c <= '9')
            l += (long) ('\\033' + c - '0');
    }
    return l;
}
```

The resulting long was converted to a string and the file was given that
name.

### Files

The files in the cache were the ones used in the [JAGGRAB protocol](./JAGGRAB-Protocol.html) (i.e. files in cache 0 in old engine caches),
 map (mX_Y), and landscape (lX_Y) files.

Incidentally, this naming is very similar to the names of the map and
landscape files in new engine caches.

## \#317 Archive Format

The old engine cache is made up two types of files.

### Data file

The data file holds all of the files in the cache and is named
`main_file_cache.dat`.
It is therefore very big, typically ~10-20MB in size.

### Index file

There are several index files, named `main_file_cache.idx` and
then post-fixed with a number.
Each index file holds 'pointers' to where a file is located in
the main cache.
Each index file represents a type of file.

### Index file format

The index file is comprised of a collection of six byte blocks which hold
information about where a file can be located in the data file.

The format of a single block is as follows:
```
tribyte fileSize
tribyte initialDataBlockId
```

### Data file format

The data file is comprised of a collection of 520 byte blocks.

The format of each of these blocks is as follows:

```
short nextFileId
short currentFilePartId
tribyte nextDataBlockId
byte nextFileTypeId
byte[512] blockData
```

### Running example

Suppose, the client wishes to fetch file type 2, file id 17.

First off, it will open the `main_file_cache.idx2` file and seek to the
index `17 * 6` (102).
It will then read the two tribytes:
```
fileSize = 1200
intialDataBlockId = 4
```

The client will now open the `main_file_cache.dat` file and seek to the
index `4 * 520` (2080).

It will then read the following:
```
nextFileId = 17
currentFilePartId = 0
nextDataBlockId = 5
nextFileTypeId = 2
blockData = ... // 512 bytes of data
```

It will read the first 512 bytes of the file and then knows that there
is 688 bytes left. 

Therefore, it has to read the next block:
```
nextFileId = 17
currentFilePartId = 1
nextDataBlockId = 6
nextFileTypeId = 2
blockData ... // 512 bytes of data
```

It reads these next 512 bytes of the file and now knows that there are
176 bytes left.

So for a final time, it will read the next block:
```
nextFileId = 18
currentFilePartId = 2
nextDataBlockId = 7
nextFileTypeId = 2
blockData = ... // 176 bytes of data
```

It can ignore most of these values (the next ones are meaningless at
this stage) and read the final 176 bytes.
The whole 1200 byte file has now been read.
