snd-soc-de1-soc-wm8731-objs := de1-soc-wm8731.o
obj-m += snd-soc-de1-soc-wm8731.o

snd-soc-opencores-i2s-objs := opencores_i2s.o
obj-m += snd-soc-opencores-i2s.o

KERNEL_SRC_DIR="/home/mib/Development/HolosynthV-Image-gen/arm-linux-4.9.33-gnueabifh-kernel/linux-4.9.33"
PWD=$(shell pwd)
CROSS_C="/home/mib/bin/gcc-linaro-5.2-2015.11-1-x86_64_arm-linux-gnueabihf/bin/arm-linux-gnueabihf-"

all:
	make -C $(KERNEL_SRC_DIR) ARCH=arm CROSS_COMPILE=$(CROSS_C) M=$(PWD) modules

clean:
	make ARCH=arm CROSS_COMPILE=$(CROSS_C) -C $(KERNEL_SRC_DIR) M=$(PWD) clean
