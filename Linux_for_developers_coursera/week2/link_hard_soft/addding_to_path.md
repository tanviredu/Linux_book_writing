we make a simple executable and add it with the path


=> cd /tmp
=> echo "echo 'this is executable'" > s


=>chmod +x s
=>export PATH=/tmp:$PATH


=>s
hello tanvir this is  script








Prepending your current directory to the path is generally a bad idea, as it makes trojan horses easy to implement.