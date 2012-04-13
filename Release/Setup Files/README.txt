
This archive contains the binary version (executable) of extcv 0.6

Homepage: http://sourceforge.net/projects/extcv/


Important
=========
You may use the binary in this archive only if you accept and agree to be 
bound by the license terms contained in the file 'License.txt', which is 
included in this archive. Full source code is available at the homepage.


Contents
========

A) Requirements for using extcv
B) Installing extcv
C) User's Guide
D) Technical details
E) Troubleshooting
F) Changelog	


A) Requirements for extcv:
--------------------------
- a Microsoft Windows operating system supported by TrueCrypt
- an installation of TrueCrypt 7.0a
- administrator rights



B) Installing extcv:
--------------------
This Software needs no installation. Just start the executable file 
'extcv.exe' included in this archive.



C) User's Guide:
----------------
The purpose of this software is to expand a TrueCrypt volume on the fly 
without reformatting. All kind of volumes (container files, disks and 
partitions) formatted with the NTFS file system are supported. The only 
condition is that there must be enough free space on the host drive or host 
device of the TrueCrypt volume.

It is also possible to expand a volume that is unformatted or formatted 
with a different file system than NTFS, but then only the TrueCrypt volume 
itself will be expanded and not the file system (if any). Passphrase 
derivation from keyfiles and legacy volumes are supported either.

Notice: shrinking a volume is not possible with this software.

WARNING: Do not use it to expand an outer volume containing a hidden 
volume, because this destroys the hidden TrueCrypt volume!

Always create a backup copy of a volume before expanding it with this 
software.


a) Expand a TrueCrypt file container:

Just start extcv.exe, select the container file of the TrueCrypt volume you 
want to expand and follow the instructions on the screen.


b) Dynamically expand a partition hosted TrueCrypt volume

With this tool, you can expand a partition-based TrueCrypt volume any later 
by adding additional hard disks. You just need to extend the host volume by 
creating a spanned volume and run this tool afterwards to expand the 
TrueCrypt volume either (spanned volumes are only supported by 
'Professional' and 'Server' editions of Windows).
  

c) Dynamically expand a RAID disk hosted TrueCrypt volume

With a hardware raid controller that allows you to extend the raid array 
dynamically, you can use this software to expand a disk-based TrueCrypt 
volume hosted on the raid device.



D) Technical details
--------------------
The expansion of a TrueCrypt volume consists of the following steps:

1) allocate disk space (only for container files)
2) fill new space with random data (if requested by user)
3) write new backup header
4) write new primary header
5) wipe old backup header
6) mount the volume
7) expand the file system (only NTFS)
8) dismount the volume

Steps 3-5 are not performed for legacy Volumes (created with TrueCrypt 4.3 
or earlier). For large volumes Step 2 needs some time to proceed (depending 
on the disk and CPU speed), all other steps only take a few seconds.



E) Troubleshooting
------------------
If an error happens, retry to expand the volume by running extcv again. If 
the problem persists, you may create a new item in the Support Requests 
Tracker at the project homepage.


F) Changelog	
------------
- Version 0.7: update to TrueCrypt 7.1a sources, requires TrueCrypt 7.1a
- Version 0.6: compatible with header version 5, requires TrueCrpyt 7.0a
- Version 0.5: initial Release (requires TrueCrpyt 6.2a)
