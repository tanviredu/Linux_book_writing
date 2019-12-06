path is  very important and critical  aspect of you environment and it is encapsulated in the 'PATH' environment variable in a centos system if we print the path variable


tanvir@localhost:/root/Storage/node_js_server_side_coursera$ echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games


when you run a command in a specfic terminal in a  specfic user this path is searched for the program and script mathed with the name

and it can be found in the 'whcich' command

so if you type

=> which vim
it will show

/usr/bin/vim

so when you type vim it will execute the command



you can  add the folder in your path


1) first make a directory in the home directory and assign with a shell variable with propoer path you can use $HOME to easily find the path


MY_BIN_DIR=$HOME/my_bin_dir

2) export it with PATH and the value $<your_path>:$PATH

export PATH=$MY_BIN_DIR:$PATH

or)	$PATH:$<your_path>

export PATH=$PATH:$MY_BIN_DIR



suppose you have a directory in the fome directory and you want to add it
then first assign it to a variable

$ MY_DIRECTORY = $HOME/my_bin_dir




another use full path variable is CDPATH

all the developer will use that

export CDPATH=/usr:CDPATH

then when you run 

=> cd /bin

it will show you the /usr/bin

Any path which begins with / is considered absolute because it specifies the exact filesystem location. Otherwise, it is considered relative and it is implicitly assumed your current directory is prepended

