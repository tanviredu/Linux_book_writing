when you doing the partition you need to consider some basic things

although it depends on the hardware it also depends on the some of the file system

1) '/boot' boot onlt hold the boot image like kernel and initrmfs file
so it should be small like 100-200 MB
and it contains the boot related partition so it is very omportnt to make this a separate partition

2) / contains everything elseso it ill be as large as need depending on the distribution system files and basic programs and development tools willtake 3.8 gb of space 

3) the swap partition should be at least double of the size of the ram

you can use a SWAP FILE inset of the swap partition but theis is a weaker method due to the stability and considaretion

so that basic partition contains three

1)/boot
2)/swap
3)/

this three partition is enough to boot a operation system

if the operatiog system in  multi user like 
multiple user using it then it is convenient to make some more

like 

1) /home directory for different users
2) /usr which is a static partition 
3) /var is  quite volatile
4) /tmp which is temporary

but one or more of this system might be avilabe only a a network share
if it used the NFS and then it is not even mountable untill the system in well-booted


you can use thr LVM partition whichis more flexible because it can create a logical volume on top of multiple physical volume

and one of the most important thing is you can dynamically
resize and move such partition