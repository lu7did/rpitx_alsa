CONFIG_MODULE_FORCE_UNLOAD=y

EXTRA_CFLAGS=-Wall -Wmissing-prototypes -Wstrict-prototypes -g -O2

obj-m += snd-rpitx.o

snd-rpitx-objs  := rpitx_module.o alsa_handling.o sysfs_variable.o iq_sample_generation.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
