# Chapter 1 - Linux Fundamentals

Here are some basic **Linux commands** you should know:

- `ls` – List files in a directory

```
ls -l   # Long format list
ls -a   # Show hidden files
```

- `pwd` – Show the present working directory

```
pwd
```

- **Clear the terminal** - `ctrl + L` to clear the terminals

### Creating, Deleting, and Reading Files in Linux

#### Create files in Linux

```
nano fileA.txt
```

```
vim fileA.txt
```

```
touch fileA.txt
```

#### Read files in Linux

```
cat fileA.txt
```

#### How to search in file in Linux

```
less fileA.txt
```

```
:/ text + enter
```

```
q // to exit
```

#### How to delete in files in Linux

```
rm fileA.txt
```

#### How to edit files in Linux

```
nano filec.txt
```

```
vi filec.txt // This will create a new file
```

```
Press esc and Shift + :
:wq
```

#### How to create a directory/folder in Linux?

```
mkdir newFolder
```

```
rm newFolder // to delete new folder
```

#### How to change path or move to another folder in Linux?

```
cd ./filepath
```

#### How to copy and paste a file from one folder to another in Linux?

```
cp ‹ file> /dest/path
```

#### How to copy content of a file to another file in Linux?

```
cp fileA.txt fileB.txt // to Create Copy
```

#### How to cut - paste a file from one folder to another in Liaux?

```
mv ‹file> /dest/path
```

#### How to rename a file in Linux?

```
mv fileA fileNewName
```

#### How to read or diplay top 5 lines from a file in Linux?

```
head -5 file
```

#### How to SORT the content from a file in Linux?

```
sort file
```

#### How to display UNIQUE content from a file in Linux?

```
// pip sign to seperate the operations
sort file | uniq

```

##### A file has 10 lines. How to split this file in 2 different files in Linux?

```
split -1 2 file
```

##### How to search a word and display matching content from a file in Linux?

```
grep "word" file
```

#### How to search multiple words and display matching content from a file in Linux?

```
egrep "word1|word2" file
```

#### How to use WILDCARDS in Linux?

\* [] {}

```
ls word*

ls *.file-extension

// it will create 5 files at once
touch file{1..5}
```

#### How to SHUFFLE content of file in Linux?

```
shuf file
```

#### How to COUNT no. of lines in a file in Linux?

```
wc -l file
```

#### How to check if two files are identical or not in Linux?

```
cmp fileA fileB
```

#### How to compare and display difference between two files in Linux?

```
diff fileA fileB
```

#### How to find a file in Linux?

```
find /path/ -name *.CSV
```

#### How to find a file in Linux?

```
updatedb

locate ‹file-name>
```

#### How to display previously used commands in past?

```
history
```

#### How to check syntax and options available for a command?

```
help
```

#### How to check which executable is using for a command?

```
which
```

#### How to check CALENDAR of last year in Linux?

```
cal
```

#### How to check How Long server has been running in Linux?

```
uptime
```

#### How to record your activity on termial in a file?

```
script

Ctrl + D // to stop the script
```

#### How to create a short-cut of a long command in Linux?

```
alias l="ls -ltr"
```

#### How to compress a file in Linux?

```
gzip -k file
```

#### How to decompress a file in Linux?

```
gzip -d file

gunzip file
```

#### How to compress a folder in Linux?

```
tar -czf myfiles.tar.gz myfiles/
```

#### How to decompress a folder in Linux?

```
tar -xzf myfiles.tar.gz
```

#### How to compress multiple files in one zipped file in Linux?

```
zip myfiles.zip filel file2
```

```
unzip myfiles.zip file.zip
```

### How to list files in zipped file?

```
unzip -l myfiles.zip
```

#### How to download a file from internet?

```
wget URL_of_file
wget -0 opt_file.txt URL_Of_file
```

#### How to call an API on Linux?

```
curl http://numbersapi.com/random
```

#### How to install an application on Linux?

```
#apt or yum/dnf
```

#### How to check if an application is installed or not on Linux?

```
rpm -qa | grep app-name
dnf list installed
```

#### How to list available packages to install on Linux?

```
apt search ‹package_name>
yum/dnf list available | grep app-name
```

#### How to start/stop a service on Linux?

```
systemctl start/stop service_name.service
```

#### How to list all services on Linux?

```
systemctl list-units --type=service --all
```

#### How to list all existing Environment Variables on Linux?

```
printenv
```

#### How to ADD a new Environment Variables permanently on Linux?

```
Add env variable in ./bashrc file

source ~/.bash_profile
```

#### How to print a specific column from a CSV file?

```
//print in vertical
awk -F '{print $2}' file.csv


//Print last columns
awk -F '{print $NF}' file.csv

//Print multiple columns
awk -F '{print $2, $3}' file.csv
```

#### How to display starting two characters of all line?

```
cut -c1-2 file.txt
```

#### How to display a specific line from a file?

```
sed -n '5p' file.txt
```

#### How to replace a specific word within a file?

```
sed 's/Rakesh/John/g' file.txt
```

#### How to convert the content to Uppercase or Lowercase within a file?

- UPPER LETTER
- lower letter
- punct: @#$%
- Digit: 12345

```
tr [:lower:] [:upper:] <file.txt
tr -d [:punct:] % <file.txt
tr [:digit:] Z <file.txt
```

```
//Replace sign with another
tr "%" "&" <file.txt
```

#### How to extend or shrink size of a file?

- ls -lh // to check the file size

```
truncate -s 10M file.txt
```

#### How to display following line in vertical line?

- ABCDE

```
echo "ABCDE" | fold -w1
```

#### How to change user or login as different user in linux?

```
su ‹user_name>
```

#### How to access remote Linux server?

- type hostname to know the host

```
#ssh user@192.168.64.3
```

#### How to copy a file to a remote Linux server?

```
scp file user@192.168.64.1:/home/pratham
```

#### How to check permissions of a file?

- r (Read) Can view the contents of the file
- w (Write) Can modify or delete the file
- x (Execute) Can run the file as a program

```
#ls -ltr
```

#### How to modify permissions of a file?

who:

- u → Owner
- g → Group
- o → Others
- a → All (Owner, Group, and Others)
- \+ → Add permission
- \- → Remove permission
- \= → Set exact permissions

```
chmod [who][+/-/=][permissions] filename

```

#### How to change ownership of a file?

```
chown root file.txt
```

#### How to change group ownership of a file?

```
chgrp paul file.txt
```

## Memory Info in Linux

#### How to check free RAM space?

```
free
free -h // shows in readable format
free -th // shows with total memory
```

#### How to check % Memory and CPU Utilization?

- press q to exit

```
top
```

#### How to check disk Utilization?

```
du
```

#### How to check filesystem available and disk space allocated?

```
df
```

### System Info

#### How to cheeck HostName

```
hostname
```

#### How to check cpu/core/thread info of your linux server?

```
lscpu
```

#### How to check type of architecture of your linux server?

```
arch
```

#### How to see list of storage devices, disk partition on your linux server?

```
lsblk
```

#### How to see OS name of linux server?

```
uname -a

cat /etc/os-release
```

#### How to check if a process(java) is running or not?

```
ps -ef | grep java
```

```
systemctl start nginx.service
systemctl stop nginx.service
systemctl status httpd.service
```

#### How to get PID of a process?

```
pgrep chron
```

#### How to stop a process by PID?

```
kill -9 PID_no
```

#### How to stop a process by its name?

```
pkill httpd
```

#### How to See Jobs in Linux

```
jobs
```

#### How to resume a job in background?

```
bg
```

#### How to run a script in background?

```
#nohup ./script >/dev/null &
```

#### How to check IP Address

```
ifconfig
```

#### How to check if a IP:PORT is accessible and open or not?

```
telnet IP Port
```

#### How to check if port is open or not on our server?

```
netstat -putan | grep 80
```

#### How to check all hubs in network path to reach a website?

```
traceroute
```

#### How to create a new gro linux server?

```
groupadd
```

#### Hot to check PID of users

```
id username
```

#### How to delete a user or group?

```
userdel ‹user>

groupdel ‹group>
```

qwqw
