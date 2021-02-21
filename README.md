# UBUNTU CLI

Package Manager
- sudo apt-get update
	- get current update able packages
- sudo apt-get upgrade
	- update all current update able packages
- sudo apt-get install filezilla
	- install filezilla
- sudo apt-get remove filezilla
	- uninstall filezilla
- sudo apt-get update
	- get lsit of package need to update

Create SSH key
- ssh-keygen -t rsa

SSH
- ssh user@192.168.1.1 -p 26
System:
- uname -a
	- System info
- blkid
	- hdd info
- top
	- task manager
- sudo shutdown -r
	- restart system
- sudo shutdown -h now
	- shutdown system now

Network:
- ifconfig
	- display network info
- iwconfig
	- display wireless network info
- ping
	- ping a server

Directory :
- pwd
	- show current dir path
- ls
	- diplay current dir contens
- ls -a
	- show all files including hidden files
- ls -l
	- show all files detail 
- ls -la
	- show all files including hidden files
	- show all files detail 
- mkdir
	- create new directory
- cd
	- change directory
	- back to home dir
- cd ..
	- back to 1 level folder
- cd /
	- back to root dir of the system (top level dir) 
- cd ~
	- back to home dir
- rmdir
	- delete a dir
- rm -R
	- delete dir and all its content

Files:
- touch filename
	- create the filename
- nano filename:
	- open the filename in nano text editor
	- cntl X to exit
	- cntl Y to save
- cat filename
	- show filename content in terminal
- less filename
	- show filename content in terminal with page down
	- cntl Q to exit
- mv filename filename2
	- rename the filename file to filename2
- cp filename2 filename3
	- make copy of filename2 and name it filename3
- cp filename2 ~/dir2/filename2
	- make copy of filename2 in dir2 directory
- rm filename2
	- delete filename2 file
- evince
	- open pdf files
- >
	- save result to a files
	- exp: ls > files1
- >>
	- append result to a new files
	- exp: ls >> files2[w 

Search and comparing files:
- grep
	- search word in files
	- exp: grep magneto File1
- diff
	- compare two files
	- exp: diff File1 File2
- which
	- search file or dir
- passwd
	- change your user password
- echo
	- display text
- VARIABLE = 
	- set value to variable
	- exp 
		- NAME = Magneto
		- echo my name is $NAME
- info
	- give description about the command
	- ctl + z to exit
- history
	- show cli history

File permission
- type:
	- u - user
	- g - group
	- o - other people
- chmod
	- change file permission
	- exp:
		- chmod o+w filename
			- return give other people  write permission on filename file.
		- chmd o-w fiiename
			- return remove other people write permission on filename file.
	- file permission
		- 0  - no permission
		- 4 - read
		- 2 - write
		- 1 - execute
		- 7 - all permission
			- exp:
				- chmod 754 filename
					- set owner have all permission on filename
					- set group have read and execute permission on filename
					- set user have only executed permission on filename

Verify download file using checksum
- sha1sum filename | gep the key number
- if return red key number and the the filename that means the download files is valid and safe.   

Compress and Decompress files
- gzip
	- compress file to zip format
	- exp: gzip filename
- gunzip
	- decompress zip files
	- exp: gunzip file.gz
- tar cvf
	- compress file to tar format
	- exp compress 2 files:
		-  tar cvf tarfilename.tar file1 file2
- tar xvf
	- decompress tar file
	- exp:
		- tar xvf tarfilename.tar

User and Group
- sudo useradd magneto
	- create new user call magneto
- sudo  passwd magneto
	- set password to magneto
- sudo groupadd xmen
	- create user group call xmen
- sudo usermod -a -G xmen magneto
	- add magneto to xmen usergroup
- sudo userdel magneto
	- delete user magneto
Setup Github
Reff: https://www.youtube.com/watch?v=ZMgLZUYd8Cw
- install:
	- sudo apt-get install git -y
- verified version:
	- git --version
- Set Up Git:
	- git config --global user.name "muhamadherwan"
	- git config --global user.email "hello.wanlab@gmail.com"
- Check account setup:
	- git config --list
