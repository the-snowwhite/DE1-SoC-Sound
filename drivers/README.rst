To build the modules out of tree, unpack/clone the kernel source from:

  $ git clone https://github.com/altera-opensource/linux-socfpga

Checkout the 4.4-altera commit:

  $ git checkout 969478b841e58aeec90fa79eb3fbd4d2a11fd57f -b 4.4-altera

Set the path to the above kernel dir in the Makefile or on the command line:

  $ ARCH=arm CROSS_COMPILE=armv7a-hardfloat-linux-gnueabi- make all

Make sure the CROSS_COMPILE string above matches your toolchain prefix.
