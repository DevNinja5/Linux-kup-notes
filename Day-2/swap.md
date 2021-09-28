## Que: What is swap space or swap memory?

Swap space is parallel space within the RAM. 
When there is no enough RAM space available, linux kernel takes some of the information from RAM and writes it to the swap space on the hard drive.
This process is swapping process.This way, your linux system can release some RAM space and doesn't crash due to lack of memory.

#### Two Swap options we can use in linux
1. Swap partition
2. Swap file

| Swap Partion | Swap File |
|-------------|------------|
| Part of your hard drive | A file alternate to partition |
| Once configured, it is not easy to change | You can modify the size of the swap file anytime, easily |
| Created at the time of installing your Linux distribution | Can be created after the installation. |

### How to check swap space
**Check swap size**
```
free -h
```
**Check swap partition size, swap type with mount point**
```
swapon
```
