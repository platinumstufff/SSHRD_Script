# SSHRD_Script
- [Nathan verygenericname's SSHRD_Script](https://github.com/verygenericname/SSHRD_Script) with some extra features
- All these extra features have been tested working on my Ubuntu PC, however there are no warranties especially for macOS, please use at your own risk
## Extra Features
- Create 10.3-11.2.6 ramdisk and mount /mnt2 on 10.3-11.2.6 devices
  - Use 10.3.x ramdisk for 10.3.x devices and 11.0-11.2.6 ramdisk for 11.0-11.2.6 devices
- Backup and restore activation files (iOS 10.3+)
  - Run `./sshrd.sh --backup-activation` to backup activation files, `./sshrd.sh --restore-activation` to restore them, both commands require booting ramdisk first
## Notes
- If there are permission denied or operation not permitted errors with sshrd.sh, try running sshrd.sh with sudo
- On 10.2.1 and lower devices, use `mount_hfs /dev/disk0s1s1 /mnt1` to mount system partition and `mount_hfs /dev/disk0s1s2 /mnt2` to mount data partition, currently idk how to copy files from/to /mnt2 on these versions
