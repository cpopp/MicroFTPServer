# uftpserver

I wanted a simple way of remotely managing files on my ESP8266 so I experimented with this minimal FTP server enough to get file listing, retrieving, and uploading working.

It's a functioning prototype now with a lot of room for improvement but it seems to work fine with the standard mac FTP client and ftp:// access via Chrome.

## Limitations
- Passive mode only
- A single data connection at a time
- Data transfer is assumed to be in binary mode (ascii setting is ignored)
- Operation blocks the thread
- No authentication support

## What is supported
- Changing directories (cd/CWD)
- Directory listing (ls/LIST with no parameters)
- File retrievals (get/RETR)
- File uploads (put/STOR) 

## Future Work
Here are some items I have in mind:
- non-blocking/callback based so it can run in the background with other scripts
- refactor the code for encapsulation purposes and to reduce memory use
- support for more commands and bit more robustness with the current ones
