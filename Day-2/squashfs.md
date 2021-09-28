## **Que 1: WHat is squashfs file system?**

Squashfs is a compressed read-only file system for Linux. 
Squashfs compresses files, inodes and directories, and supports block sizes from `4 KiB` up to `1 MiB` for greater compression.

> Inodes in the system are very small and all blocks are packed to minimise data overhead. Block sizes greater than 4K are supported up to a maximum of 1Mbytes (default block size 128K).
