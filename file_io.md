- The dd command allows you to easily create test files with file sizes of your choice. 
- The tee command allows you to print output to screen while also writing it to a file
- Installing a new hard disk partition:
    1. Install physical disk 
    2. Check to see if physical disk is recognized by system: fdisk -l
    3. Create a new partition: fdisk /dev/sdc
    4. Verify partition type (id should be 83 for linux): fdisk /dev/sdc
    5. Format disk using the partition type of your choice: mkfs.ext4 /dev/sdc
    6. Obtain the UUID of the new partition: blkid
    7. Add new partition to /etc/fstab
    8. Mount new partition