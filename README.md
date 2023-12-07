DAHDI Linux Complete
====================
DADHI Linux Complete is a full package that consists of both DAHDI Linux
and DAHDI Tools.

This is a simple-to-install 'complete' DAHDI kit for Linux users. It is
designed to be a drop-in replacement for users used to building
Zaptel for their system without specifying any special build options,
file locations, or anything else.

If one need to influence the build or installation process in any way
outside the defaults, user will need to use the installation steps
specific to the dahdi-linux and dahdi-tools packages separately
(both of which are located in subdirectories of the dahdi-complete package).


Pre-Requisites:

For Redhat:

yum -y install kernel-devel-$(uname -r) libtool* make gcc patch perl bison gcc-c++ ncurses-devel flex flex-devel libtermcap-devel autoconf* automake* autoconf
yum -y install gcc ncurses-devel libtermcap-devel kernel-devel gcc-c++ newt-devel zlib-devel unixODBC-devel libtool make

For Debian:

apt-get -y install gcc g++ automake autoconf libtool make libncurses5-dev flex bison patch libtool autoconf linux-headers-$(uname -r) sqlite3 libsqlite3-dev
apt-get -y install gcc libncurses-devel kernel-devel kernel-smp-devel gcc-c++ libnewt-dev zlib-devel unixODBC-devel libtool make

To install this package, execute these commands:

Step 1)

$ make all

This will build the dahdi-linux kernel modules for your
currently-running Linux kernel, and the dahdi-tools userspace tools.

Step 2)

$ make install

You will need to run this step as root (or via sudo or some
equivalent), to install the kernel modules and userspace tools on your
system.

Step 3 (optional))

$ make config

Again you will need to run this step as root or equivalent; this step
is only needed if you want to install the sample DAHDI configuration
files and init script and have not previously installed them.

