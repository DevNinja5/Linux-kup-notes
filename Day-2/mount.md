## Que: How to mount a file system?

To mount a file system on device we use mount commands.

For example:

`mount [OPTION...] DEVICE_NAME DIRECTORY`

```
sudo mount /dev/sbd2 /mnt/usb
```
Usually when mounting a device it auto-detect common file system such as ext4 or xfs.
To specify file system type use `-t` option

```
sudo mount -t ext4 /dev/sbd2 /mnt/usb
```
