
[when i say memory i mean the RAM and the swap (virtual memory )not THE HARDDRIVE]

[memory means RAM and SWAP not harddrive]

[all the memory related file in the '/proc' directory]

linux use something called virtual memory system (VM) as like allthe mordan operating system.interesting thing is the virtual memory is larger that the physical memory

each of the process has its own ,protected space. the address they are using are virtual and must be transalted to the physical address by the kernel

why kernel cause kernel handles the hardware and make avilabe for software use 

with the kernel the process acces the memory

the process send the virtual memory to the kernel kernel tranlet the proces into the physical memory and then execute it

but its anoher interesting thing is kernel itself uses the virtual memory

the memory translation depend on the architecture and the type of the memory that is used


kernell gives enough memory to the allocated running process . and coordinate when a memory is sharing by multiple process.mapping can be used to linka  file directly to process virual addess apce for using that location.and certain process can be protected against writing or code execution


to see the memory we use a  command called 

=>free -mt


[root@localhost boot]# free -mt
              total        used        free      shared  buff/cache   available
Mem:            991          71         797           6         121         774
Low:            991         193         797
High:             0           0           0
Swap:          2047           0        2047


so we have total 991MB memory (RAM)
and we have SWAP (2GB)

remember theswap memory is used for backing up the ram
if you dont have the swap memory or stop the swap memory
and the process exceds the memory use it will suddenly kill the whiole process


you can turn the swap off by using this command

=>sudo /sbin/swapoff -a

you can turn the swap on by using this command

=>sudo /sbin/swapon -a

[when tou write this command the swap will not instantly removed it takes a little time to reduce down to zero]


there are another memory called cache memory

cache memory hold the data in the cache memory .the data that you recently accessed to free the cache memory this command is used

=>free -m
=>su root
=>echo 3 /proc/sys/vm/drop_cache
=>exit (exit from the root aaccount)
=>exac bash [to make the change effect]

// check account
=> free -mt




to see the detail information about the memory

cat /proc/meminfo

it is important that to remember that application directly dont write the storage such media as disk directly they interface with the virtual memory system and these virtual data blocks are placed into buffer or cache then they are flushed into the disk when convenient and necessary in the most of the system the caching layer then the physical layer thats why we say virtual memory is grater than the physical memory
 



 we say that Linux employes a virtual memory system in which the operating system can function as if it had more memory than it really does.
 

 but why?? why we try to think there are more virtual memory then actual there it is??

 1) Many programs do not actually use all the memory the are given permission to use .sometimes is because the clield process inherit a copy of parent memory utilizing (COW) (copy on Write).so the cliend process only get the copy when there is a change


 2) when memory pressure become high we have swap space that is a part of the hard drive but we still consider them as  a memory (RAM)


 						Process and Threads
--------------------------------------------------------------------------

Inm Linux there are a lot of process that are continuously running and they 
contain and produce a lot of information


why there are a need a threaded process??

so some times a program need to do same thing for multiple user or multiple task at the same time

like if you running a web server your server may have multiple client and for this multiple client your server can run multiple session that does the same job but for different different users. this called session hence thread this threads have the same process id. because multi threaded program share same files and resources.and multithreaded program can do multiple things

there are lot of way to make a multi threaded program but the standerd way of making muti threaded program is to use the POSIX Threads or the (pthreads) library

although it says that if you use the POSIX standerd tou will get a complete portability but in Practical it is not .it is a good idea that you test it




REMEMBER ONE THING MEMORY USED BY THE KERNEL NEVER SWAPPED OUT NEVER?
KERNEL DONT USE THE SWAP

AND THE OOM(OUT OF MEMORY) TRY TI KILL THE PROCESS THAT USE EXCESS MEMORY THAN SUPPLIED AND TYY TO KEEP RUNNING THE SYSTEM