KPATH := /usr/src/linux-headers-`uname -r`

obj-m := ./src/iomemmap.o

.PHONY: all clean doc

all:
	make -C $(KPATH) M=$(CURDIR) modules

clean:
	make -C $(KPATH) M=$(CURDIR) clean
	rm -rf ./doc

doc:
	doxygen ./Doxyfile
