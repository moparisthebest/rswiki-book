# Ondemand protocol

The Ondemand protocol is used to stream updates to the cache.
The client knows which files to update from the CRC file downloaded
using the [JAGGRAB Protocol](./JAGGRAB-Protocol.html).

## Request format

The client first authenticates as an ondemand client by using the opcode
'15' (as opposed to the game, which uses the type '14').

The format of the request is:

```
unsigned byte cacheId;
unsigned short fileId;
unsigned byte priority;
```

Furthermore, there can be multiple requests per session.

## Response format

The response is sent in blocks. The maximum size of a block is 500
bytes. Smaller blocks (e.g. towards the end of a file) are permitted.

The format of a block is:
```
unsigned byte cacheId;
unsigned short fileId;
unsigned short fileSize;
unsigned byte blockNumber;
unsigned byte[] blockData;
```
