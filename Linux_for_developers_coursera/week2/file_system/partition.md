under the linux disk are divided into partitions the term slices is not often used

that means actually  the total storage is sliced or we call it partitions


there are primary partitions and extended partitions

you can make highest four primary partitions
and the information like master boot record store there but it is not flexible

if you make three primary partition and on eextended partition then it will be more flexible

the extended partition can hold a smany logical partition as required
but it is also depended in the hardware that you are using

for example there are SCSI drive can hold 16 partition



the uNIC kernel can hold all the  pre-attached hard disk durinf system boot and there are no configuration file required to inform about what is present


but in the hotplug system the udev system will find the disk unpon the insertion in the system and read the partition table

to create a disk partition and modify it we use the fdisk utility



=>sudo /sbin/fdisk -l


[REMEMBER YOU CAN MAKE PARTITION AND REMOVE IT WITH fdisk BUT CAN NOT RESIZE OR MOVE IT]

to increase the file size

with 

=> resize2fs

partition can be formatted using this following command

=> sudo mkfs -t ext4 /dev/sda10

=> sudo mkfs.ext4 /dev/sda10



you can use the gparted tools for the partition




make partitions 

1) first see the block devices using the 
=>lsblk 

2) fdisk /dev/sd[your block device name]

3) press m for help [it will show all the possible commands]

4) p means print all the partition

5) n for new
	-> select the primary
	-> take defaut
	-> add the size with +5G for 5 gigabyte [your choice]
	-> then 'L' for the partition type
	-> 83 is the standerd linux partiotion
	-> write change the 'w'
	-> partprobe <partition> to activate it

6) add the file system mkfs.ext4 <partition>