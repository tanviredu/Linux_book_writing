all the service that is currently running
	->systemctl
all the avilable service
	->systemctl list-units -t service -all
start a service
	->systemctl start <service>
stop a service 
	->systemctl stop <service>
enable(start at runtime) service
	->systemctl enable <service>
disable service
	->systemctl disable <service>
see the status of the service
	->systemctl status <service>

you can do it in some machine with the chkconfig on|off command