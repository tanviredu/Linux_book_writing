cd bin
ldd PackerTracer


it will show the installed and missing packages


download the packages manually like for libpng12

after downlaod it
run

dpkg -x libpng12-0_1.2.50-2+deb8u3_amd64.deb  ./out
then copy the dependency no need to install

cp ./out/lib/x86_64-linux-gnu/libpng12.so.0 /opt/packettracer/bin/


if other is mission install them too
