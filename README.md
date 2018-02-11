![](http://aparapi.com/images/logo-text-adjacent.png)

```
git submodule init
git submodule update
./prepare.sh
libtoolize (or sometimes glibtoolize on osx)
aclocal
autoconf
automake --add-missing
./configure
make
```

Shared library in `.libs/libaparapi.dynlib` for osx and `.libs/libaparapi.so` for linux.

To prepare a 32bit version on a 64bit Linux system simply run configure as:
./configure --build=i686-pc-linux-gnu "CFLAGS=-m32" "CXXFLAGS=-m32" "LDFLAGS=-m32"

# OSX

Make sure JAVA_HOME is set properly. One way to set it is as follows

```bash
$ nano -w ~/.bash_profile

export JAVA_HOME=$(/usr/libexec/java_home)
```
