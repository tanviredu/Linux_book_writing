1) to bring a network connection to live and give it a ip address

	suppose the ip address is :192.168.0.100
	and the interface is eth0
	the command is
	=>sudo /sbin/ifconfig <interface> <ip>
	=>sudo /sbin/ifconfig eth0 up 192.168.0.100

2) to bring a network connection to live and give dynamic address [connecting to the dhcp server]

	
	interface is eth0
	the command is:
		=>sudo /sbin/dhclient <interface>
		=>sudo /sbin/dhclient eth0

3) to see the status and the network address and interafce
	the command is
		=>ifconfig

4) to see the status and the network address and interafce
	the new  command is
		=> ip addr show
	to see the interface of the connection
		=>ip link


		to see the "ifconfig" like output with the ip command is

		=>ip -s link show <interface>
		=>ip -s link show eth0

5) bring a connection to live  adding an ip address with the ip command

	=> ip addr add <ip> dev <interface>
	=> ip addr add 192.168.0.100 dev eth0

6) bring eth0 down
	=>ip link set <interface> down
	=>ip link set eth0 down

7) setting the MTU
	=>ip link set mtu <value>
	=>ip link set mtu 14500
8) setting the route
	=> ip route add <address/subnet> via <gateway>
	=>ip route add 192.168.0.100/24 via 192.168.0.1




