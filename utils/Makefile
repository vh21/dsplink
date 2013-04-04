.PHONY: all install

BINDIR := build/tmp-angstrom_v2012_05-eglibc/work/beagleboard-angstrom-linux-gnueabi/ti-dsplink-1_1_65_00_03-r122j/dsplink_linux_1_65_00_03/dsplink
DESTDIR := /media/Angstrom/usr/share/ti/ti-dsplink-examples/ 

GPPBIN := gpp/BUILD/LOOP/BIN/RELEASE/loopgpp
DSPBIN := dsp/BUILD/OMAP3530_0/LOOP/BIN/RELEASE/loop.out


all:
	bitbake ti-dsplink -f -c compile
	bitbake ti-dsplink -f -c build


install:
	sudo cp $(BINDIR)/$(GPPBIN) $(DESTDIR)
	sudo cp $(BINDIR)/$(DSPBIN) $(DESTDIR)
	sudo cp runloop /media/Angstrom/usr/bin/
	sudo cp setupdsp /media/Angstrom/usr/bin/
	sync
	eject /dev/sdb
