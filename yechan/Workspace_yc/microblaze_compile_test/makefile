# Makefile to build select Microblaze projects.


BIN_PMOD = pmod_oled.bin

all: iop_bins
	@echo
	@tput setaf 2 ; echo "Completed Microblaze Projects' Builds"; tput sgr0;
	@echo

iop_bins: $(BIN_PMOD)
	@cp */Debug/*.bin .

%.bin: FORCE
	cd $(subst .bin,,$@)/Debug && make clean && make 

clean:
	rm -f */Debug/*.bin
	rm -f */Debug/*.elf
	rm -f */Debug/*.elf.size
	rm -f */Debug/src/*.o
	rm -f */Debug/src/*.d
	rm -f *.bin
	rm -rf .Xil .metadata SDK.log	

FORCE: