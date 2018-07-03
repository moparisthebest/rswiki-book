\[\[Category Cache\]\]

== Introduction ==

The JAGGRAB protocol is used to 'grab' cache files from the file server
and download them.

It is a text-based protocol, similar to HTTP/0.9, and the client will
fall back to HTTP if JAGGRAB is unavailable. This generally happens in
unsigned mode and helps users who are behind firewalls.

== Request format ==

A request is simply the text JAGGRAB, a space, the path to the file and
a newline character. Therefore, it is very similar to a HTTP/0.9 GET
request.

JAGGRAB /path/to/file

=== New engine ===

In (perhaps all) new engine clients, the client prefixes the JAGGRAB
request line with a single byte (value 17).

== Response format ==

The response is simply the raw file data. Once the response is sent, the
connection is closed.

== Files ==

There are a number of files which map to files in the cache.

-   '''/crc''' - the CRC table
-   '''/title''' - cache 0, file 1
-   '''/config''' - cache 0, file 2
-   '''/interface''' - cache 0, file 3
-   '''/media''' - cache 0, file 4
-   '''/versionlist''' - cache 0, file 5
-   '''/textures''' - cache 0, file 6
-   '''/wordenc''' - cache 0, file 7
-   '''/sounds''' - cache 0, file 8

NOTE: the client will usually postfix these with random numbers, so when
checking for the file only the start of the string should be examined:
not the whole one. This is to help avoid caches when these files are
fetched over HTTP.<BR> NOTE: The crc is postfixed with the client
revision
