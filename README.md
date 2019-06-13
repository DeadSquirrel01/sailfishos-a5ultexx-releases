Sailfishos sources for a5 are not in github, but in my gitlab here: https://gitlab.com/Marco01

Releases can be downloaded at https://github.com/DeadSquirrel01/sailfishos-a5ultexx-releases/releases

What works: everything except audio on fm radio

How to install:

1) Install lineage 14.1 from the release.<br/>
Note: you have to install the lineage 14.1 in sailfish release and not the one in xda, otherwise the hardware that has text relocation libs e.g camera and audio will not work!<br/>
2) Install sailfishos zip.<br/>
3) Reboot

How to install OTAs for Sailfish 3.0 and higher:

1) Open terminal and log in as root by running "devel-su" command. You can set root password in "Settings app -> Developer tools"<br/>
2) Run "zypper ref" to update packages metadata<br/>
3) Run "zypper dup" to install device and sailfish OTA updates<br/>

How to update Sailfish 3.0 and higher to next release:

1) Open terminal and log in as root by running "devel-su" command. You can set root password in "Settings app -> Developer tools"<br/>
2) Run "ssu re NEWER_RELEASE" i.e. "ssu re 3.0.3.10" to upgrade repos to 3.0.3.10<br/>
3) Run "version --dup" to upgrade the system to the release you specified with "ssu re" command
4) Reboot

<b>NOTE</b>:<br/>
To upgrade sailfish, don't install a newer SailfishOS zip, follow the instructions above, otherwise you will lose all your personal data.<br/>
SailfishOS zips are for users who don't have it installed and installing newer ones doesn't have to be taken as a way to upgrade the system, like in android ROMs.<br/>
While you don't have to upgrade the system by installing newer sailfish zips, it is recommended to update sailfishos' lineage 14.1 to latest release's one

How to run SailfishOS as secondary ROM with multirom:

1) Download multirom zip and recovery from latest release<br/>
2) Install multirom recovery with odin (or unpack the tar and install the img) and multirom zip with recovery<br/>
3) Reboot to recovery, go in "multirom menu -> Add ROM -> SailfishOS" and select "sailfishos's" lineageos 14.1 zip as "CyanogenMod ZIP file" and sailfishos zip as "Rootfs ZIP file"
4) Proceed to their installation
5) Move	/sdcard/MultiROM/multirom/roms/YOUR_SAILFISH_ROM_NAME/data/.stowaways directory in /data. After that, make sure you have /data/.stowaways/sailfishos/... 
6) Inject boot sector from multirom menu in recovery

Changelog<br/>
https://github.com/DeadSquirrel01/sailfishos-a5ultexx-releases/blob/master/changelog.txt
