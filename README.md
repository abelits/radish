Radish
======

Root filesystem generator and installer for Linux.

This set of scripts is implements Linux system installation from a running (potentially unrelated) Linux system.

    radish-build

produces a root filesystem image from packages taken from the distribution's repository. There are three arguments, all optional. First argument is the Debian or Ubuntu release name passed to debootstrap, second argument is the kernel release for LTS version of Ubuntu -- it is ignored for Debian. For example,

    ./radish-build precise quantal

will produce a root filesystem image for Ubuntu 12.04 (Precise Pangolin) with backported Linux kernel 3.5 from Ubuntu 12.10 (Quantal Quetzal). By default, the release is Debian 7.x (Wheezy) with its original kernel (updated to the last available version).

The third optional argument is the URL for the Debian or Ubuntu mirror that is used for installation. If the second argument is not used, it should be "". For example,

    ./radish-build yakkety "" http://archive.ubuntu.com/ubuntu

will produce a root filesystem image for Ubuntu 16.10 (Yakkety Yak) from a repository located at http://archive.ubuntu.com/ubuntu .


    radish-install

installs the image on a removable drive, produces configuration files for this instance of the Linux system, generates boot filesystem and installs the bootloader.

The current version can be used to install Debian or Ubuntu on a USB (or other removable) drive.
