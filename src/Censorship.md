# Censorship

Chat message censorship is applied client-side.

Traditionally, the use of bad words does not always result in a punishment,
unless if applied manually by a staff member.

## Process

There are four related cache files which are loaded and used in censorship.

They are as follows:

| Cache file name | Purpose |
|---|---|
| `fragmentsenc.txt` | ? |
| `badenc.txt` | Contains bad words, including variations (e.g. `fuck`, `fok`, etc.). |
| `domainenc.txt` | Contains bad domain names. |
| `tldlist.txt` | Contains possible top-level domain names. |

When an input is received, if bad phrases are found they are replaced
with a sequence of astericks.

Bad phrases are either a bad word, or a combination of a bad domain name and a top-level domain name.
