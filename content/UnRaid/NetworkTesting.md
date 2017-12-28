---
Title: Network Testing
Description: Various methods for testing the network throughput
Sort: 1
---
1. On say the synology box
````bash
    mkdir /x
    mount //tower2/<share> /x -o user=nobody
    time cp /x/path/to/big/file /dev/null
    umount /x
```` 
    In the end divide total size of the file by "real" time to get transfer rate.


