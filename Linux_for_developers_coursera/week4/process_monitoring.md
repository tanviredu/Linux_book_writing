linux system comes with many standerd performance and profiling tools that is already installed some of them may be familier with other unix system 
there may be other system that can used only in linux


all the tools are gatharing the information from the /proc file system

cause all the process information stored in the psudo file system named
	/proc

	there are also graphical tools for that

	->gnome-system-tools for (GNOME)
	->ksysguard (FOR KDE) (you can use it to another desktop environment without any problem)
	-> inred hat yopu need to install the
		1)ksysguard
		2)ksusguardd 

		it has some advantage
			1)gnome-system-monitor has no savinf functionality but ksysguard has
			and you can save it as a worksheet
			2) you can monitor other system in that
				this can be done with ssh protocols
				it will luch the ksysgurdd daemon in that system and with the client we can monitor other system
			3) i can set the window display and workspace which is not avilable in the gnome-system-monitor



				install ksysguard in redhat
					->sudo yum install ksysguard*
					on suse linux
					->sudo zypper install kdebase4-workspace
					in debian/ubuntu
					->sudo apt install ksysguard


