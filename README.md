# SSHRD_Script
- [Nathan verygenericname's SSHRD_Script](https://github.com/verygenericname/SSHRD_Script) with some extra features
- All these extra features have been tested working on my Ubuntu PC, however there are no warranties especially for macOS, please use at your own risk

## Extra Features
- Create 10.3-11.2.6 ramdisk and mount /mnt2 on 10.3-11.2.6 devices
  - Use 10.3.x ramdisk for 10.3.x devices and 11.0-11.2.6 ramdisk for 11.0-11.2.6 devices

## Notes
- It is recommended to run sshrd.sh with sudo
- On 10.2.1 and lower devices, use `mount_hfs /dev/disk0s1s1 /mnt1` to mount system partition and `mount_hfs /dev/disk0s1s2 /mnt2` to mount data partition
