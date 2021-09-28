## Que : Why ext4 file system is faster than other linux file systems?

Ext4 introduces a lot of improvements in the ways storage blocks are allocated before writing them to disk,
which can significantly increase both read and write performance.

It supports **Delayed Allocation**


For example 
> when a process is writing continually to a file that grows, successive write()s allocate blocks for the data, but they don't know if the file will keep growing. 
> Delayed allocation, on the other hand, does not allocate the blocks immediately when the process write()s, rather, it delays the allocation of the blocks while the file is kept in cache, until it is really going to be written to the disk. 
> This gives the block allocator the opportunity to optimize the allocation in situations where the old system couldn't.
