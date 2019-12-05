environment variable are not limited in length or number
lot of applicaion use the environment variable
to set the default value for 


Remember Environment variable is used to set the default value
you can use

HOME
HOST
PATH
and can be set as  PATH

[remember putting the ./ in front of the path is a very security risk
because this is used to execute the binary
]


to make a environment variable

1) usually we use capital letter to make make environment variable
	like EDITOR=/bin/vi

	you dont have to use double quote

2) but it still does not work unless you export it

	export EDITOR

3) how to use the ENVIRONMENT variable??

	use   $ before the name before you call then

	like $EDITOR




prompt for the shell

for regular shell we use the '$'

and for the root shell we use the '#'

customize the shell prompt

ypu may think why this thing even necessary

yes it is necessary at least thrre things should have in the shell prompt

1) machine name(hostname)
2)the username
3)the current directory

to make this thing 
make a environment variable name PS1
PS1="\h:\u:\w"

this is because
\t -> for time
\d -> date
\s -> shell name
\w -> current directory
\u -> User
\h -> Hostname
\\# -> command number
\! -> history


you can customize the shell prompt using this


there are other things that a shell find special

>  is used for redirect the output
<  is used to redirect the input
>> append the input
>&	redirect the stout and stdrr

| is used for piping

suppose you want to make a command is a separate shell
the command will be enclosed by a vracket

(command)

&&   this is called and it is used for concatening command
;	 this is for separating command

{}	is for list

~ is used for redirecting the home directory

`  backtick is used for expression

$(()) areticmitic substiution

[] wild card ecpression

&  background job
# used for comments

*? Used in expansion wild card
!	Usedin history




