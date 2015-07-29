Enhancing Device::USB has been a little difficult due to differences in the [libusb](http://libusb.wiki.sourceforge.net/) libraries for different operating systems. Linux is pretty straight-forward. The libusb version 0.1 or newer is available on most distributions and works with Device::USB out of the box.

Windows variants have been much harder because libusb is not supported. There is a port of libusb to Windows [libusb-win32](http://libusb-win32.sourceforge.net/), but I don't have a development system to do the port at this time.

We have had some luck with Mac OSX. The main issue appears to be the libusb that comes installed is not compatible. The trick appears to be to go to [libusb at SourceForge](http://libusb.wiki.sourceforge.net/) and get the latest version from Subversion or CVS. Follow the instructions to compile libusb. Device::USB should now install without any difficulty.

StrawberryPerlInstallation now documents the steps to install Device::USB on [Strawberry Perl](http://strawberryperl.com).