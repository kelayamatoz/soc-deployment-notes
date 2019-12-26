# Managing Partitions
By default, the linux image only consumes ~7 GB of the total SD card capacity. To utilize the full SD card, one can add another partition, and add the following line into /etc/fstab. This way, Linaro will mount the partition at /media/storage when the device boots:
```bash
/dev/mmcblk0p4 /media/storage vfat defaults 0 0
```

We assume that the new partition is at /dev/mmcblk0p4. One can always use lsblk for further checking.