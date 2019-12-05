File Description:

remember a command has three type of discryption
1) input (standared input) numeric value is 0
2) output (standered outpur) numeric value is 1
3) error (if error occur) numeric value is 2

suppose we want to run the ls command 

ls take the url as  a parameter
this url is a input
so this command can be implemented with this

ls < 'location'
ls < '/root'


suppose you want to redirect the output

ls '/root' > output.txt

also

ls '/root' 1 > output.txt

if the command is successfull

if you want to redirect the error in a specfic file for logging purpose
then

ls '/path/dontexists' 2 > error_log.txt

this will only store the error



piping the value through other command


suppose you want to find a directory name file1 in the current directory

ls | grep file1

suppose x=3

echo $x+1	 will output 3+1
echo $(expr $x+1) output 4
echo $((x+1))	output 4


expr is not basically used

$(()) this is is the mordan command


suppose the 

ls /etc/passwd

ls /etc/passwd_not

first file will show the output
and second command will be be an error cause this command does not exists



1) redirect normal output a file and error another file
ls /etc/passwd  /etc/passwd_not >stdout_out 2>stderr_out

to other 

command to redirect to the same file

ls /etc/passwd /etc/passwd_not > logdile.txt 2>&1

it means the first command output will be stored into the logfile
and the second output will be point to the same file the first command goes


other way
ls /etc/passwd /etc/passed-not >& log

ls /etc/paswd /etc_passwd_not 




ans of the question
---------------------
which add a newbin a direcory to home directory?
-----------------------
PATH=$HOME/newbin/$PATH
--------------------
$echo $(expr $x - 3)
$echo $(($x - 3))
------------------
foo >& file
foo >file 2>&1
------------------
alias doitall="make clean; make all; evince output.pdf"