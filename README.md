# SSHRD_Script
- [Nathan verygenericname's SSHRD_Script](https://github.com/verygenericname/SSHRD_Script) with some extra features
- All these extra features have been tested working on my Ubuntu PC, however there are no warranties especially for macOS, please use at your own risk
## Extra Features
- Create 10.3-11.2.6 ramdisk and mount /mnt2 on 10.3-11.2.6 devices
  - Use 10.3.x ramdisk for 10.3.x devices and 11.0-11.2.6 ramdisk for 11.0-11.2.6 devices
- Backup and restore activation files (iOS 10.3+)
  - Run `./sshrd.sh --backup-activation` to backup activation files, `./sshrd.sh --restore-activation` to restore them, both commands require booting ramdisk first
- Backup and restore the entire contents on NAND
  - Run `./sshrd.sh --dump-nand` to backup NAND to disk0.gz, `./sshrd.sh --restore-nand` to restore disk0.gz to /dev/disk0 on device
  - Both commands are supposed to be executed directly after device entered DFU mode
- iOS 7-8 brute force (partially supported)
  - Run `./sshrd.sh --brute-force` to get unlimited passcode attempts on passcode locked and disabled devices, iOS 7-8 only
  - Directly run this command after device entered DFU mode
  - A7 iOS 7 devices will be stuck in recovery loop after booting iOS 12 ramdisk, you may boot an iOS 8 ramdisk using [Legacy iOS Kit](https://github.com/LukeZGD/Legacy-iOS-Kit) to fix this, which is not supported by SSHRD_Script
## Notes
- If there are permission denied or operation not permitted errors with sshrd.sh, try running sshrd.sh with sudo
- On 10.2.1 and lower devices, use `mount_filesystems -h`
