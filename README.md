Radish
======

Root filesystem generator and installer for Linux.

This set of scripts is implements Linux system installation from a running (potentially unrelated) Linux system.

    radish-build

produces a root filesystem image from packages taken from the distribution's repository.

    radish-install

installs the image on a removable drive, produces configuration files for this instance of the Linux system, generates boot filesystem and installs the bootloader.

The current version can be used to install Debian Wheezy on a USB (or other removable drive). There should be less hardcoded and more configurable parameters in the future.
