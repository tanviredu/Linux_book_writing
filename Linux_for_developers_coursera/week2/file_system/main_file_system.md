this things have to be remember
'/' is the root directory all the directory wil be inside it
and all the direcoty and 
	
		is it in  FHS standard -> yes

'/bin' directory tll the essential exucatable programs that must be avilable for
		"SINGLE USER MODE" will be in side the /bin directory


		is it in  FHS standard -> yes

[all the single user executable will be there]


'/boot ' this is a very important directory .the files that are needed to boot such as 

	1) kernel
	2) initramfs
	3) boot confguratio file
	stays here

	is it in  FHS standard -> yes

'/etc' this is the directory where system wide configuration file stored
	
	is it in  FHS standard -> yes

'/home ' all the home content including the personal file stored here

	is it in  FHS standard -> yes

'/lib' libraries required by the  executables called /bin and /sbin stored here

	is it in  FHS standard -> yes

'/lib64'  all the 64 bit libraries stored here. all the 32 bit and 64 bit stores here

	is it in  FHS standard -> NO

'/media' this is actually for a mount point such as CD and USB disk

	is it in  FHS standard -> yes

'/mnt' this is for mounting and  using the temporary file system,
	
	is it in  FHS standard -> yes

'/proc' this is the thirf party software goes
	
	is it in  FHS standard -> yes

'/sys' this is not a file system .its psudo file system it give all the information about the system and the process running on it. it is used to alter system parameters

	its not a real file system

	is it in  FHS standard -> NO

'root' -> home directory for root(super user) user

	is it in  FHS standard -> YES

'/sbin' system binaries for the system

	is it in  FHS standard -> YES

'/srv' sire specfiv data this is not used most of the time

	is it in  FHS standard -> YES

'/tmp' temporary files stored here it can configured many distribution used as a ramdisk memory

	is it in  FHS standard -> YES


'/var' all the logging file stored .you want log thats where you got it
	
	is it in  FHS standard -> YES



if a system can be able to boot and go into single user or recovery mode with only

1) /bin
2) /sbin
3) /etc
4) /lib
5) /boot




the most interesting directory can be /usr and /var

'/usr/bin' non essential binaries and script not needed for the single user mode.that means it is not necessary to boot the system

'/usr/include' all the header file used here to cmpile the code

'/usr/lib' Libraries for /usr/bin and /usr/bin

'/usr/lib64' Libraries for /usr/bin and /usr/bin only yhe 64 bit

'/usr/sbin' non essential system binaries such as system deamons

'/usr/share' Shared data from application

'/usr/src' SOURCE CODE FOR THE LINUX KERNEL

'/usr/X11R6' x window system files

'/usr/local' Local data for the specficly to the host stored here



'/Var' directory is used for a lot of thing 

'/var/ftp' it is used for the ftp server base

'/var/lib' Persistent data modified by the program they run

'/var/lock' Lock files to control simultanious program

'/var/log' Log files

'/var/mail' this is the user mailbox

'/var/run' information about the running since the last boot

'/var/spool' task that is spooled for the queue to be processed especially like the machine printter

'/var/www' this is where the web server resource go