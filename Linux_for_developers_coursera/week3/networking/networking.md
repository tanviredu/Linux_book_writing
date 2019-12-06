The vast majority of networ programming in linux is done using the socket interface.There are many inhancement in the network inr linux has introduced.such as new kinds of address and protocol families for 
example linux offers netlink interfce whgich permits openning  up the socket connection between kernel subsystem and application

in linux the wired connection is is known etho and eth1 etc and the wireless devices is named like wlan0 and wlan1

linux also have advance firewall and selinux interface for controlling network traffic and network service

there are two most used command to see the network address and status

=> ip addr show

=> ifconfig

the tools is under the 

=> /sbin/ifconfig

the if config tools can be obtain by the  net-tools command



$ /sbin/ifconfig
eth0      Link encap:Ethernet  HWaddr 00:22:15:2B:64:A6
          inet addr:192.168.1.100  Bcast:192.168.1.255  Mask:255.255.255.0
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:163529 errors:0 dropped:0 overruns:0 frame:0
          TX packets:112693 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:183642176 (175.1 MiB)  TX bytes:12101864 (11.5 MiB)
          Interrupt:18
eth1      Link encap:Ethernet  HWaddr 00:22:15:2B:63:BE
          inet addr:192.168.0.101  Bcast:192.168.0.255  Mask:255.255.255.0
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:162597 errors:0 dropped:0 overruns:0 frame:0
          TX packets:56710 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:206698846 (197.1 MiB)  TX bytes:75532637 (72.0 MiB)
          Interrupt:17
          
lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          UP LOOPBACK RUNNING  MTU:16436  Metric:1
          RX packets:15115 errors:0 dropped:0 overruns:0 frame:0
          TX packets:15115 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:126793920 (120.9 MiB)  TX bytes:126793920 (120.9 MiB)





      information that is displayed include the hardware MAC (media access controll) address and MTU (MAximum Transfer unit) and also shows the number of packet that is sending and reciving

      the machine has two network cards both eth0 and eth1 and the loopback address lo.
      the loopback address is used to connect to the service within the machine




      you can see the statstical information by looking at this file

      => ls -l /sys/class/net/eth0/statstics

      -r--r--r--. 1 root root 4096 Dec  6 10:32 collisions
-r--r--r--. 1 root root 4096 Dec  6 10:32 multicast
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_bytes
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_compressed
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_crc_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_dropped
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_fifo_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_frame_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_length_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_missed_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_nohandler
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_over_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 rx_packets
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_aborted_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_bytes
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_carrier_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_compressed
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_dropped
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_fifo_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_heartbeat_errors
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_packets
-r--r--r--. 1 root root 4096 Dec  6 10:32 tx_window_errors




all the files contains the value of each of the parameter





				using predictable connection
	--------------------------------------------------


naming the networ ninterface eth0 and eth1 can be problametic when multiple interface exists .there should be a systematic approach for naming them

many system administrator have solvedthis problem in a simple manner

there is a mordan approach is offered by the Predictable Network Interface Device Name Scheme which is strongly correlated with the use of udev and integration with systemd


Udev is the device manager for the linux kernel that creates and removes devicesm nodes from the /dev directory dynamically and it support hotplug and with the help of the udev user can gives names to the connected devices using the udev rules


there are five types of names that can be given
->Using BIOS provided index number for on-board devices like en01 (on board network card)
->Using BIOS provided PCIExpress hotplug slot  ens1 (addditional network card/pci express)

->Using the Geographical location of the hardware connection like enp2s0

->using the direct MAC address enx7837dlea46a

-> using the old method eth0

it is very easy to turn of the new scheme and use the old one