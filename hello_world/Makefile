# Makefile – makefile of our first driver

# if KERNELRELEASE is not defined, we've been called directly from the command line.
# Invoke the kernel build system.
ifeq (${KERNELRELEASE},)
	KERNEL_SOURCE := /usr/src/linux-headers-3.11.0-15-generic
	PWD := $(shell pwd)
# Otherwise KERNELRELEASE is defined; we've been invoked from the
# kernel build system and can use its language.
else
endif
	obj-m := ofcd.o
default:
	${MAKE} -C ${KERNEL_SOURCE} SUBDIRS=${PWD} modules

clean:
	${MAKE} -C ${KERNEL_SOURCE} SUBDIRS=${PWD} clean

