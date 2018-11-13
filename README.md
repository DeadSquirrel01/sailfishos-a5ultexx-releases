Sailfishos sources for a5 are not in github, but in my gitlab here: https://gitlab.com/Marco01

Releases can be downloaded at https://github.com/DeadSquirrel01/sailfishos-a5ultexx-releases/releases

What works: everything except audio on fm radio

How to install:

Install lineage 14.1 from the release.

Note: you have to install the lineage 14.1 in sailfish release and not the one in xda, otherwise the hardware that has text relocation libs e.g camera and audio will not work!

Install sailfishos zip.

Reboot

How to install OTAs for Sailfish <= 3.0:

1) Open terminal and log in as root by running "devel-su" command. You can set root password in settings-> deve
2) Run zypper ref to update packages metadata
3) Run zypper dup to install device and sailfish OTA updates

TODO: upload multirom with sailfish support and his instructions
