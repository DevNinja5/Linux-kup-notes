## Que : What are /dev/loopx and /dev/ttyx ?

**/dev/loop**
> In Unix and Linux-like operating systems, files are accessible as block files using loop devices. 
> These devices have no concern with RAM occupation in the system. 
> The dev loop is also termed as vnode disk (vnd) and loopback file interface (lofi).

The `/dev/loop` devices treat files with a filesystem image as if they were block devices. The loop devices are snaps because snap packages are created that way.

These files were containing a filesystem that is mounted to the location. 
It is an approach that developers use to pack an entire package in a single file, but the operating system access all the files. 
The approach used here is therefore known as loop mounts.


**/dev/tty**
