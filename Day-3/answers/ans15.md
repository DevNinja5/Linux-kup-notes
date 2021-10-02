# Que 15: What does the number represent after the file permissions?

**Command**
```
ls -l
```
Output
```text
drwxr-xr-x 6 knoldus knoldus     4096 Oct  2 20:57  Desktop
drwxr-xr-x 2 knoldus knoldus     4096 Sep 16 11:06  Documents
drwxr-xr-x 6 knoldus knoldus     4096 Oct  2 00:07  Downloads
drwxrwxr-x 2 knoldus knoldus     4096 Aug 30 13:31  IdeaProjects
drwxrwxr-x 2 knoldus knoldus     4096 Sep  5 18:51  javasharedresources
-rw-rw-r-- 1 knoldus knoldus 39214560 Dec  4  2018  kubectl.1
drwxr-xr-x 2 knoldus knoldus     4096 Jul 24 13:47  Music
drwxr-xr-x 3 knoldus knoldus     4096 Aug 25 18:48  node_modules
-rw-r--r-- 1 knoldus knoldus      249 Aug 25 18:48  package-lock.json
drwxr-xr-x 3 knoldus knoldus    12288 Sep 29 18:54  Pictures
drwxrwxr-x 3 knoldus knoldus     4096 Aug  3 17:14  project
drwxr-xr-x 2 knoldus knoldus     4096 Jul 24 13:47  Public
drwxr-xr-x 6 knoldus knoldus     4096 Jul 29 23:38  snap

```
`6` in `drwxr-xr-x 6` means number of directories present in this directory including `.` & `..`
