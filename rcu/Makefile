obj-m := rcu.o 

KERNELDIR := /lib/modules/$(shell uname -r)/build
PWD := $(shell pwd)
all:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules
ccflags-y += -Wall
ccflags-y += -Werror

default:
	$(MAKE) -C $(KDIR) SUBDIRS=$(PWD) modules

install:
	insmod rcu.ko
remove:
	rmmod rcu.ko
clean:
	rm -rf *.o *.ko *.mod *.symvers *.order *.mod.c
