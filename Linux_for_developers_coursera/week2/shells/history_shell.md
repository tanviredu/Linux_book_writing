most linux users uses bash shell

bash stands for bourne again shell

there are other shell
1)sh
2)csh
3)tcsh
4)ksh
5)bash

1)sh is written by the Steve Vourne at AT&T and 1977
this is known as the Bourne shell
it is avilable in all the system

2)csh -> it is written by the UC barkly it is different than sh and its 
syntax is like the  c programming language thats why it is called c shell

3)tchs is the enhanced version of the csh shell
t stand s for TENEX ,TENEX is a operations system
that is previously used but now a  days mohst of the time csh is a link of
the tcsh because we only use the enhanced version

4) ksh is stands for korn shell it is preety compatable in sh but it has 
 a lot of new features the shell is very very favourate in the system administrator

5)bash -> bash stands for bourn again shell its a product of the GNU
its a major upgrade of the sh  and full backward compatability with sh and partial compatability with ksh

6)zsh is the another shell has  a lot og extended features
z shell is fairly new shell and but it is not widely used

on most of the system sh is just a  link to bash
but the script that are invoked by the sh with only work
with out the bash
similler relationship applied to tsh and csh
so if you want to run some thing with sh it will not load the bash extension

porting script between sh,ksh and bash is relatievely easy and straight forward

porting csh is littlebit complecated


bash and ksh offer a enhanced redability compared fue to the sh extension.
the bash and ksh runfaster that other


the newer shell adapt some of the externam commnads into their default one
such as /bin/echo command is now just echo


kind of shell

1) login shell
2) interactive shell
3) non interactive shell

1)a login shell is one requiring a password (for loggin in)
2)a inyteractive shell is one which the standered input and output connected to the terminal 
3)A non-interactive shell is one in which the standered input that is connected to process .it will start a process not give you the instant reply

most distribution include an system-wide-file usually
/etc/bashrc from the users !/.bashrc






bash alias

some times we alias a big or other command for easy use
unalias will remove all the alias

alias l="ls -lF"
alias dir='ls -latf'
alias rm='rm -i'
alias mv='mv -i'
alias cp='cp -ipdv'
alias df='df -T'
alias mygoogle='firefox https://www.google.com'