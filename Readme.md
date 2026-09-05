# Start-Of-Packet

A general purpose binary protocol that enables you to parse your data starting at any point in a stream.  With just 8 bytes of overhead per packet it uses a "start of packet" field and a checksum to define your payload.

| Byte Range | Description |
| ---------- | ----------- |
| 0 - 1 | Start of packet - [0x37, 0x10] |
| 2 | Version - 0x00 |
| 3 | Payload id |
| 4 - 6 | 24 bit payload length |
| 7 | 8 bit header crc |
| .. | Payload |
