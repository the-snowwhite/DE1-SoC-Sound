PREFIX  = $(CROSS_COMPILE)
CC      = $(PREFIX)gcc
CXX     = $(PREFIX)g++
CPP     = $(PREFIX)cpp
LD      = $(PREFIX)gcc
AR      = $(PREFIX)ar
RANLIB  = $(PREFIX)ranlib

SRC := $(shell pwd)
KERNEL_SRC ?= $(HOME)/my_stuff/home/hardware/terasic/linux-socfpga

obj-m += snd-soc-opencores-i2s.o
obj-m += snd-soc-de1-soc-wm8731.o

all:
	$(MAKE) -C $(KERNEL_SRC) M=$(SRC)

modules_install:
	$(MAKE) -C $(KERNEL_SRC) M=$(SRC) modules_install

clean:
	rm -f *.o *~ core .depend .*.cmd *.ko *.mod.c
	rm -f Module.markers Module.symvers modules.order
	rm -rf .tmp_versions Modules.symvers

