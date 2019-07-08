Sailfishos sources for a5 are not in github, but in my gitlab here: https://gitlab.com/Marco01

Releases can be downloaded at https://github.com/DeadSquirrel01/sailfishos-a5ultexx-releases/releases

What works: everything; nfc works in lineage 14.1 but hasn't been tested on sailfish.<br/>
If you find issues, please report them in "issues" page

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
SailfishOS zips are for users who don't have it installed and installing newer ones doesn't have to be taken as a way to upgrade the system, like in android ROMs

How to run SailfishOS as secondary ROM with multirom:

1) Download multirom zip and recovery from latest release<br/>
2) Install multirom recovery with odin (or unpack the tar and install the img) and multirom zip with recovery<br/>
3) Reboot to recovery, go in "multirom menu -> Add ROM -> SailfishOS" and select "sailfishos's" lineageos 14.1 zip as "CyanogenMod ZIP file" and sailfishos zip as "Rootfs ZIP file"
4) Proceed to their installation
5) Move	/sdcard/MultiROM/multirom/roms/YOUR_SAILFISH_ROM_NAME/data/.stowaways directory in /data. After that, make sure you have /data/.stowaways/sailfishos/... 
6) Inject boot sector from multirom menu in recovery

Changelog<br/>
https://github.com/DeadSquirrel01/sailfishos-a5ultexx-releases/blob/master/changelog.txt

<b>IMPORTANT!</b>

You will have to flash a RIL-fix zip to make RIL working. <br />
If your variant is SM-A500FU, you will not have to flash any RIL-fix zip! <br />
RIL zip contains device-specific libsec-ril.so and libsec-ril-dsds.so, if the device supports dual sim. <br />
Here are the RIL-fix zips. Make sure you install the one corresponding to your variant!

For normal sailfish users: <br />
[ril fix A500F.zip](https://drive.google.com/file/d/1Un7jyNg-al1fXWICyv_B3bHa971rgMLC) (SM-A500F) <br />
[ril fix A500F1.zip](https://drive.google.com/file/d/1pl411Cg2z__uVZtvO0HBZ4SS8rseLDA7) (SM-A500F1) <br />
[ril fix A500G.zip](https://drive.google.com/file/d/1PN8AxCteE0mmS3OR9G9kKixX550BRtez) (SM-A500G) <br />
[ril fix A500H.zip](https://drive.google.com/file/d/1cF--hVihvcHtxVLKX8qpRbQwcvC4d6vK) (SM-A500H) <br />
[ril fix A500K.zip](https://drive.google.com/file/d/1BiCvSav2FdvTLOvSSVFkiy_GUCFS4tiL) (SM-A500K) <br />
[ril fix A500L.zip](https://drive.google.com/file/d/1WqLA68Y37PzH4ceuFhfGxJC5gfl2FpHK) (SM-A500L) <br />
[ril fix A500M.zip](https://drive.google.com/file/d/15RYkvXgRBx2Ea2s2n6AO3qwPM9ywxjTj) (SM-A500M) <br />
[ril fix A500S.zip](https://drive.google.com/file/d/1LgXW7rFfg2_Fgz1RLZcXVcCzqt57DZAD) (SM-A500S) <br />
[ril fix A500W.zip](https://drive.google.com/file/d/1j2U0IQq0GtbIin3fqJHiMGDD5PE54jUA) (SM-A500W) <br />
[ril fix A500Y.zip](https://drive.google.com/file/d/1pQL7RqQvSerb6nYR5lBSwDwADSi2YlQ7) (SM-A500Y) <br />
[ril fix A500YZ.zip](https://drive.google.com/file/d/1MRW_LL2aiTuWQAwdzcX9Xz6-eizTqjCc) (SM-A500YZ)

For multirom users (lineage 14.1 installed in /data/.stowaways/sailfishos) <br />
[ril fix A500F-mrom.zip](https://drive.google.com/file/d/1MvK07k2w9ZexgLM6PDekg-T_Xv9DpWwp) (SM-A500F) <br />
[ril fix A500F1-mrom.zip](https://drive.google.com/file/d/1pzFVJilQLRwomrDRSO5T_AOhET1Drohu) (SM-A500F1) <br />
[ril fix A500G-mrom.zip](https://drive.google.com/file/d/1x4CmuEBKznFsfyUadQTiSZ2nxzZFa0KX) (SM-A500G) <br />
[ril fix A500H-mrom.zip](https://drive.google.com/file/d/1s15lOCdMtWdLYIEWzVChRFRQU2Qdfk8e) (SM-A500H) <br />
[ril fix A500K-mrom.zip](https://drive.google.com/file/d/1UwQaMfmc997nS9Uo_wU9mpLUX7qqXdwH) (SM-A500K) <br />
[ril fix A500L-mrom.zip](https://drive.google.com/file/d/1CYFDAeBBsyyvmHY9_jVpPSAhECGJZETr) (SM-A500L) <br />
[ril fix A500M-mrom.zip](https://drive.google.com/file/d/1Ox_rbAE-0OHtrSSeukDDldlvW7NlXGln) (SM-A500M) <br />
[ril fix A500S-mrom.zip](https://drive.google.com/file/d/1MQyjad0XL3473eIw4RYt1SyCXnPUDEGo) (SM-A500S) <br />
[ril fix A500W-mrom.zip](https://drive.google.com/file/d/1klVlLhGqOm4ki8Hz1bk-FOovFiFxKhlr) (SM-A500W) <br />
[ril fix A500Y-mrom.zip](https://drive.google.com/file/d/1Nuy-KsS13HKHbzV7s6AKr636_YN2K65U) (SM-A500Y) <br />
[ril fix A500YZ-mrom.zip](https://drive.google.com/file/d/1gK2RQo6kSiB4hdDUBLOaUN9qC7HpAKbh) (SM-A500YZ)
