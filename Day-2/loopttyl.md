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

`/dev/tty` is a special file, representing the terminal for the current process.
> `/dev/tty` stands for the controlling terminal (if any) for the current process. To find out which tty's are attached to which processes use the `ps -a` command at the shell prompt (command line). Look at the "tty" column.

**Output will look like:**
```text
    PID TTY          TIME CMD
   6682 tty2     00:22:27 Xorg
   6699 tty2     00:00:00 gnome-session-b
 113596 pts/0    00:00:00 ps

```
