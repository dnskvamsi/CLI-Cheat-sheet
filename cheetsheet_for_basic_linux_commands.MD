# <center>  Cheatsheet_for_basic_linux_commands </center>

## <center> PWD </center>
### pwd
> #### It dispay's the current working directory.
---
## <center> cd </center>
### cd
> #### cd stands for change directory. It is used to navigate to specific folder.
#### Syntax:-
> #### cd \<path>


> #### Eg:-cd /home/user, cd ./../../home

>#### To navigate to home we can use.
> #### cd ~, cd $HOME, cd 

### cd -
> #### It is used to navigate to the previous working directory.

## <center> mkdir </center>
### mkdir
> #### Make directory. It is used to create a new directories.

#### Syntax:-
> #### mkdir \<dirname1> \<dirname2>  . . . . 
> #### Eg:- mkdir d1, mkdir d1 d2 d3 , mkdir .dir1(creates hidden directory).
### mkdir d{1..4}
> #### It creates directories d1, d2, d3 and d4.
### mkdir -p dir1/dir2
> #### -p flag is used to create parent directory if it doesn't exists.

## <center> rmdir </center>
### rmdir
> #### remove directories. It is used to remove existing empty directories.

#### Syntax:-
> #### rmdir \<dirname1> \<dirname2>  . . . . 
> #### Eg:- rmdir d1, rmdir d1 d2 d3.
### rmdir d{1..4}
> #### It removes directories d1, d2, d3 and d4.
### rmdir -p dir1/dir2
> #### -p flag is used to remoe parent directory too if it parent is empty.

## <center> ls </center>
### ls
> #### List the files and directores. It is used to print all the files and folders present.

#### Syntax:-
> #### ls \[options] \<path Name>
> #### Eg:- ls . , ls /home
#### ls -a
> #### It prints all the files and directories including the hidden files and folders.
#### ls -l
> #### -l flag for long listing.It prints all the files permissions, size, name, owner name, group name..etc
#### ls -t
> #### -t flag is used to print all the files as per modified time of files and directories.
#### ls -lh
> #### h stands for human readble format. It prints all the file sizes in the human readle format.
#### ls -R
> #### R stands for Recursive. it prints all the files and folders recursively.
#### ls -r
> #### -r stands for reverse order.It prints all the files and folders in reverse order.
#### ls -alrht
> #### we can combine all the options and this provides all the functionality of a ,l,r,t,h

## <center> cp </center>
### cp
> #### cp stands for copy.Copy the files from one location to another. It doen't delete the original file. (it internally works as cat source>destination).

#### Syntax:-
> #### cp \[option]  \<source>  \<destination>
> #### Eg:- cp file1 file2, cp file1 /home/file1.
### cp file1 file2 file3 dir1
> #### It copies file1,file2,file3 to dir1(directory)
### cp -r dir1 dir2
> #### -r tag is used to recursively copy the dir1 to dir2.

## <center> mv </center>
### mv
> #### mv stands for move.moves the files from one location to another. It cuts from source location and paste in the destination location.

#### Syntax:-
> #### mv \[option]  \<source>  \<destination>
> #### Eg:- mv file1 file2, mv file1 /home/user
### mv file1 file2 file3 dir1
> #### It moves file1,file2,file3 to dir1(directory).

## <center> rm </center>
### rm
> #### rm stands for remove.delete the files.

#### Syntax:-
> #### rm \[option]  \<file1> \<file2> \<file3> . . .
> #### Eg:- rm file1, rm file1 file2 file3
### rm -r dir1
> #### It removes the entire directory recursively.
### rm -f file1
> #### It forcefully deletes the file1.

## <center> chmod </center>
### chmod
> #### This is used to change file or directories permissions. By default the permissions are 774. You can check using umask.

#### Syntax:-
> #### chmod \[option]  \<file1> \<file2> \<file3> . . .
> #### Eg:- chmod 777 file1 , chmod u-x file1 ..
### chmod ugo-rwx file1
> * #### u stands for user permissions
> * #### g stands for group permissions
> * #### o stands for other permissions
> * #### r stands for read permission (4)
> * #### w stands for write permission (2)
> * #### x stands for executable permission (1)
> #### The commands removes all the permissions for the file1
### chmod g-x file1 file2
> #### it removes the executable permission from group of file1 and file2.
### chmod -r  g-x dir1
> #### it recursively removes the executable permissions from the group to all the subfiles and folders.
### chmod ug=rw file1
> #### it sets read,write permissions to user and group.
### chmod 776 file1
> #### it sets read,write,executable permissions to user and group. but it sets only read and write to others.
> * #### 7 (r+w+x== 4+2+1)
> * #### 6( r+w == 4+2 )
### chmod g+x file1 file2
> #### it adds the executable permission to group for file1 file2 

# <center> chown </center>
### chown
> #### chown stands for change owner it changes the owner of a file to another file.

#### Syntax:-
> #### chown \<ownerName> \<filename>  . . . . 
> #### Eg:- chown owner1 f1, chown owner2 f1 f2
### chown -r owner1 dir1
> #### It recursively changes the owner of all the subfiles and folders.

# <center> sudo </center>
### sudo
> #### some files do not have the privilages to view and modify then we use sudo we can modify those as sudo(root) user has all the privilages to view and modify.

#### Syntax:-
> #### sudo command
> #### Eg:- sudo cat /etc/passwd , sudo  apt-get install htop.

# <center> apt </center>
### apt
> #### apt is a repository where you find all the package. using apt we install the package from our command line.

#### Syntax:-
> #### sudo apt \[task] \<package Name>
> #### Eg:- sudo apt install htop, sudo apt install git.

### apt install \<packageName>
> #### It install's the package which we have specified.

### apt uninstall \<packageName>
> #### It uninstall's the package which we have specified from the local system but the .deb file will not be deleted.

### apt remove \<packageName>
> #### It uninstall's and deletes the package which we have specified from the local system but some of configuration files are left over.

### apt purge \<packageName>
> #### It uninstalls and deletes the entire package and it also deletes the configurations files which are related to the package.

### apt update
> #### It looks for updates for the installed applications and updates all the applications.


### apt upgrade
> #### It is used to upgrade the packages or( application) which are present in the local system.