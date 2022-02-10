# Android Debug Bridge

## Geräteinformationen

````sh
$ getprop | grep .version

[gsm.version.baseband]: [G920FXXU5EQJ2]
[gsm.version.ril-impl]: [Samsung RIL v3.0]
[net.knox.shareddevice.version]: [2.6.0]
[net.knoxscep.version]: [2.1.1]
[net.knoxsso.version]: [2.5.0]
[net.knoxvpn.version]: [2.3.0]
[persist.service.bdroid.version]: [4.2]
[ro.build.scafe.version]: [2017A]
[ro.build.version.all_codenames]: [REL]
[ro.build.version.base_os]: []
[ro.build.version.codename]: [REL]
[ro.build.version.incremental]: [G920FXXU5EQJ2]
[ro.build.version.preview_sdk]: [0]
[ro.build.version.release]: [7.0]
[ro.build.version.sdk]: [24]
[ro.build.version.security_patch]: [2017-10-01]
[ro.build.version.sem]: [2402]
[ro.build.version.sep]: [80000]
[ro.com.google.gmsversion]: [7.0_r8]
[ro.config.iccc_version]: [1.0]
[ro.config.timaversion]: [3.0]
[ro.opengles.version]: [196610]
[ro.security.reactive.version]: [2.0.11]
[security.ASKS.policy_version]: [161228]
[security.ASKS.version]: [1.4]
[selinux.policy_version]: [SEPF_SECMOBILE_7.0_0005]
[sys.config.mars_version]: [2.00]
[sys.enterprise.billing.version]: [1.2.0]
[sys.enterprise.otp.version]: [2.6.0]
````

## In anderen Modus booten

````sh
$ adb reboot [bootloader|recovery|sideload|sideload-auto-reboot]
````

## Partitionen finden

````sh
$ cat /proc/mounts
rootfs / rootfs ro,seclabel 0 0
tmpfs /dev tmpfs rw,seclabel,nosuid,relatime,size=1372976k,nr_inodes=343244,mode=755 0 0
devpts /dev/pts devpts rw,seclabel,relatime,mode=600 0 0
proc /proc proc rw,relatime,gid=3009,hidepid=2 0 0
sysfs /sys sysfs rw,seclabel,relatime 0 0
selinuxfs /sys/fs/selinux selinuxfs rw,relatime 0 0
/sys/kernel/debug /sys/kernel/debug debugfs rw,seclabel,relatime 0 0
none /acct cgroup rw,relatime,cpuacct 0 0
tmpfs /mnt tmpfs rw,seclabel,relatime,size=1372976k,nr_inodes=343244,mode=755,gid=1000 0 0
none /config configfs rw,relatime 0 0
none /dev/cpuctl cgroup rw,relatime,cpu 0 0
pstore /sys/fs/pstore pstore rw,seclabel,relatime 0 0
/dev/block/dm-0 /system ext4 ro,seclabel,relatime,norecovery 0 0
/dev/block/platform/15570000.ufs/by-name/EFS /efs ext4 rw,seclabel,nosuid,nodev,noatime,discard,journal_checksum,journal_async_commit,noauto_da_alloc,data=ordered 0 0
/dev/block/platform/15570000.ufs/by-name/CACHE /cache ext4 rw,seclabel,nosuid,nodev,noatime,journal_checksum,journal_async_commit,noauto_da_alloc 0 0
/dev/block/platform/15570000.ufs/by-name/USERDATA /data ext4 rw,seclabel,nosuid,nodev,noatime,journal_checksum,journal_async_commit,noauto_da_alloc 0 0
/dev/block/platform/15570000.ufs/by-name/PERSDATA /persdata/absolute ext4 rw,seclabel,nosuid,nodev,noatime,discard,journal_checksum,journal_async_commit,noauto_da_alloc,data=ordered 0 0
/dev/block/platform/15570000.ufs/by-name/SBFS /sbfs ext4 rw,seclabel,nosuid,nodev,relatime 0 0
tmpfs /storage tmpfs rw,seclabel,relatime,size=1372976k,nr_inodes=343244,mode=755,gid=1000 0 0
/dev/block/platform/15570000.ufs/by-name/HIDDEN /preload ext4 ro,seclabel,nosuid,nodev,relatime,data=ordered 0 0
/data/knox/tmp_sdcard /mnt/knox sdcardfs rw,nosuid,nodev,relatime,mask=0077 0 0
/data/knox/sdcard /mnt/knox/default/knox-emulated sdcardfs rw,nosuid,nodev,relatime,low_uid=1000,low_gid=1000,gid=1015,multi_user,mask=0006 0 0
/data/knox/sdcard /mnt/knox/read/knox-emulated sdcardfs rw,nosuid,nodev,relatime,low_uid=1000,low_gid=1000,gid=9997,multi_user,mask=0027 0 0
/data/knox/sdcard /mnt/knox/write/knox-emulated sdcardfs rw,nosuid,nodev,relatime,low_uid=1000,low_gid=1000,gid=9997,multi_user,mask=0007 0 0
/data/knox/secure_fs/enc_media /mnt/shell/enc_media sdcardfs rw,nosuid,nodev,relatime,low_uid=1000,low_gid=1000,gid=9997,multi_user,reserved=20MB 0 0
/data/media /mnt/runtime/default/emulated sdcardfs rw,nosuid,nodev,noexec,noatime,low_uid=1023,low_gid=1023,gid=1015,multi_user,mask=0006,reserved=20MB 0 0
/data/media /storage/emulated sdcardfs rw,nosuid,nodev,noexec,noatime,low_uid=1023,low_gid=1023,gid=1015,multi_user,mask=0006,reserved=20MB 0 0
/data/media /mnt/runtime/read/emulated sdcardfs rw,nosuid,nodev,noexec,noatime,low_uid=1023,low_gid=1023,gid=9997,multi_user,mask=0027,reserved=20MB 0 0
/data/media /mnt/runtime/write/emulated sdcardfs rw,nosuid,nodev,noexec,noatime,low_uid=1023,low_gid=1023,gid=9997,multi_user,mask=0007,reserved=20MB 0 0





$ cat /proc/partitions
major minor  #blocks  name

 253        0    2097152 vnswap0
   8        0   31240192 sda
   8        1       4096 sda1
   8        2       4096 sda2
   8        3      20480 sda3
   8        4       8192 sda4
   8        5      28672 sda5
   8        6      34816 sda6
   8        7       8192 sda7
   8        8      43008 sda8
   8        9       1024 sda9
   8       10       1024 sda10
   8       11        768 sda11
   8       12        256 sda12
   8       13       9216 sda13
   8       14      15360 sda14
   8       15    3788800 sda15
 259        0     204800 sda16
 259        1      51200 sda17
 259        2   27004928 sda18
   8       16       4096 sdb
   8       32       4096 sdc
 254        0    3755992 dm-0
````

## Dateien vom / auf's Gerät kopieren

````sh
$ adb pull <PATH>

$ adb push <LOCAL-PATH> <ANDROID-PATH>
````

## Partitionen sichern

````sh
adb pull /dev/block/mmcblk0 ./data/mmcblk0.bin
````

## ADB Shell $\Rightarrow$ Superuser

````sh
$ adb shell

zeroflte:/ $ su
zeroflte:/ # 
=> Root access
````

## Dateipfade

**App Data:** `/data/data/<APP-ID>`
**Partitionen:** `/proc/partitions`

## Sicherung mit ADB via netcat

### Terminal 1

````
1. $ adb shell

4. $ mount
5. $ dd if=<path> vs-2048 conc=noerror,sync | nc -l -l 5555
````

### Terminal 2

````
2. $ adb forward tcp 5555 tcp 5555
3. cd <path>
6. <AUS FOLIEN CHECKEN>
````
