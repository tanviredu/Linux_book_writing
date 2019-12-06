here are three main types of devices
	1) character devices
	2) block devices
	3) network devices

Character devices are used to perform/implement the open,close,read,write function to a serial port 
	1)terminal /dev/tty (yes tyerminal is a devices too)
	2)printer /dev/pl1 
	3) sound card /dev/dsp0

Block devices are readonly accessed I/O operation like filesystem for example hadrdrive
	1)/dev/sda
	2)/dev/cdrom

Network devices like transmission and reviception with socket interface.transfer packet data in blocks and streams
	1) ethernet eth0
	2) wireles wlan1

Othe types devices like USb devies or SCSI


these devices shares a underlying protolcols regardless of function
the main challange is writing the driver

there are also user-space drivers but there are nit efficient as  kernel-drivers
user-space drivers works in the user space

like linux printing drivers

Devices are generally placed under the /dev directory

=>sudo mknod -m /dev/name <type> <major> <minor>
=> mknod -m 666 /dev/mycdrv c 254 1

major numer shows the driver with the devices and all the devices in the same node

minor number shows the derivative
	-> can be different instance of same devices like first and second sound carf
	-> different model

	posix wants to have  a major and minor number in the 


	udev create the node on the fly when needed and remove when disconnected
	and it gives persisten name 

	udev runs as a daemon and monitor a netlink socket

	for udev to function we need the 
		1) libudev library
		2) udevd that manages the /udev direcory
		3) devadm utility to controll and diagonistics


udev support hotplug

the configuration baseed on the 
	1) permision
	2) mounting point
	3) ownership
	are stored in the /etc/udev/udev.conf file
	the udev rules is located in /etc/udev/rules.d

	udev ->user device manager

	you cant get rid of the major and minor number for posix standered