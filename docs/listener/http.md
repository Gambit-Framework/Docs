# Gambit HTTP Listener Protocol

## Pawn -> Server

```txt
Session Id      [8 Bytes]   // session id
Code            [1 Byte]    // 0 = Register, 1 = Checkin, 2 = Task Result
Size            [8 bytes]   // size of data section
Status          [1 byte]    // 0 = success, 1 = error
Data            [X Bytes]   // task result or error message
```
