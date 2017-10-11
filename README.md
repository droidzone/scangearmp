#SCANNING SOLUTION FOR CANON G2000 using SANE

This ScanGear MP provides scanning functions for Canon Multifunction Inkjet Printer. 

Thierry HUCHARD added support for Canon G2000 scanning support

###How to install package:

git clone git@github.com:droidzone/scangearmp.git

cd scangearmp/scangearmp/

autoreconf -vfi

cd ../

sudo apt install libsane-dev libtool-bin libusb-dev

debuild -tc

Dont worry if you see a "debsign: gpg error occurred!  Aborting....debuild: fatal error at line 1295:running debsign failed" line at the end. That's normal.

This will generate a debian package in ../ named something like ../scangearmp-common_2.30-1_amd64.deb

Install with:

sudo dpkg -i ../scangearmp-common_2.30-1_amd64.deb

Test with:
scanimage -L

If successful, it will tell you that: "device `pixma:04A91795_1019CD' is a CANON Canon PIXMA G2000 multi-function peripheral"
