# Copyright (C) 2019 Logitech

VENDOR=Logitech
PROJECT_NAME=G613_Receiver
VERSION=RQR43.01_B0009
FIRMWARE_FILES=../RQR43.01_B0009.shex
METAINFO_FILES=com.logitech.RQR43.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm -f *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
