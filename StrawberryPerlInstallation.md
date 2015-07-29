# Introduction #

Although the Device::USB project was orignally developed on Linux, this has not stopped Windows developers from wanting to access their USB devices. [Strawberry Perl](http://strawberryperl.com/) actually makes this fairly easy.

# Pre-Requisites #

Before installing Device::USB, you will need a few other things first.

  1. Install [Strawberry Perl](http://strawberryperl.com/)
  1. Install the [libusb-win32](http://libusb-win32.sourceforge.net/) library
  1. Install the [Inline::C](http://search.cpan.org/search?query=Inline%3A%3AC&mode=module) Perl module

If you are on this page, you have probably already accomplished step 1. The second step provides the library needed to talk to USB hardware of all types. Device::USB provides a Perl wrapper for this library.

Step three is needed in order to do an installation with an Inline::C module.

# Installation #

Once you have the pre-requisites taken care of, the installation is really straight-forward.

Since Windows does not really have a standard directory structure for include files and libraries, we need to tell the Device::USB installation where to find these files for libusb-win32.

  1. For Strawberry Perl, installation is normally performed from a command line. So you need to open a command (or DOS) window.
  1. Create or change to a short directory without spaces in the name. Spaces in the directory name causes problems with the **cpan** program.
```
    cd C:\TEMP
```
  1. The Device::USB installation code gets this information from two environment variables: **LIBUSB\_INCDIR** and **LIBUSB\_LIBDIR**. If you installed libusb-win32 in the default location, you can use the lines below:
```
    set LIBUSB_INCDIR=\Program Files\LibUSB-Win32\include
    set LIBUSB_LIBDIR=\Program Files\LibUSB-Win32\lib\gcc
```
  1. Install Device::USB with **cpan**
```
    cpan Device::USB
```

This should complete successfully and Device::USB will be available. An easy test is to use perldoc to verify that the POD has been installed.

```
    perldoc Device::USB
```