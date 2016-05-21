###Run Level
There are 7 levels in linux:
* level0: poweroff
* level3: terminal mode
* level5: GUI mode
* level6: restart
init [level] to switch level, for example, type "init 0" to shut down computer.

###Document type
Everything in linux is file/document, including hardware.

* d:directory
* -: regular file, ASCII/binary/data,etc
* l: link file
* b: block device
* c: character device
* s: sockets
* p: pipe

###File permission command
* chgrp: change group
* chown: change owner
* chmod: change permission

###Document permissions

# file
* r: read content of file
* w: modify/edit contentof file, not including deleting the file
* x: file can be executed by this user.

# directory
* r: list the file and subdir of the directory, that is, user can use "ls" command to list all files and subdirs of the direcotry
* w: modify the content of directory,that is, add/delete/rename/move files and subdirs of directory.
* x: user can use "cd" command to make the directory as work directory. 
###### warn: if user has "r" permission to a directory, it doesn't mean user can change directory to this directory.


####File System
1. Three type area
    * superblock: record overall filesystem information, including total count,used count, remained count of  inode/block
    * inode: record file/directory attribute, such as permission, owner, group, etc, typically, inode area will record address of block area,just like pointer in C, by which computer can locate the real data of a file/directory. Each inode has same capacity, such as 128/256 bytes. 
    * block: record data of file/directory
2. EXT2 and FAT
 Exts is called indexed allocation file system, whose inode area record all block area addresses, while FAT is linked allocation file system, whose block area can be reached one by one, like a linked list.


