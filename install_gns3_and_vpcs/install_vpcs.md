cd /tmp
svn checkout svn://svn.code.sf.net/p/vpcs/code/trunk vpcs-code
cd vpcs-code/src
rgetopt='int getopt(int argc, char *const *argv, const char *optstr);'
sed -i "s/^int getopt.*/$rgetopt/" getopt.h
unset -v rgetopt
sed -i 's/i386/x86_64/' Makefile.linux
sed -i 's/-s -static//' Makefile.linux
make -f Makefile.linux
strip --strip-unneeded vpcs
sudo mv vpcs /usr/local/bin
