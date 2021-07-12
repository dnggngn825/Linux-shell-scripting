# Linux-shell-scripting
This is based on the Intro to Linux Shell scripting online course on Udemy
## Definition
A Shell script is a text file that contains a series of commands and shell statements when a shell script is executed it in turn executes the commands listed in teh script that starts at the very top and executes the commands on each line one line at a time until the end of the file.

Executing a shell script produces the exact same result as you typing in each line directly into the terminal, any work we can do on the command line can be automated by a shell script and the converse is true as well.

### Text editors
- Vim
- emacs
- Nano (need to install first)

### Install Nano
For Debian based Linux distribution, Ubuntu
```bash
sudo apt-get install -y nano
```

-------------------------------

### Create a first script
```bash
nano day1.sh
```
We can name the shell script anything and the script's end in ```.sh``` is not significant like it is in some other operating system

Then just type in the content in the script, hit ```Ctrl + X``` to save change and hit ```Y```
```bash
#!/bin/bash
echo "I dont have to be great to start, but I have to start to be great!"
```
It will ask for filename, just press ```Enter``` and we will get our first script file. Now, to run the file, we first have to give it permission to run by using command ```chmod``` which means 'change mode', ```+x``` gives the file the execute permission
```bash
chmod +x day1.sh
```
or
```bash
chmod +rx day1.sh
```
gives the permission to read and execute for the shell script

then
```bash
./day1.sh
```
which outputs
```bash
Hello World
```
### File name does not matter then what matters?
It turns out that the file permission matters and more specifically, the shell script needs to have executable permissions, which can be viewed using ```ls``` shell command
```bash
ls -l
```
which returns
```bash
-rwxr-xr-x 1 dangnguyen dangnguyen 88 Jul  3 23:59 day1.sh
```
where ```-rwxr-xr-x``` stands for permission string. The first character in the string ```-``` tells
if it is a file (```-```) or a directory (```d```). The next three tells the permission granted of the file (R stands for read, W stands for write and X stands for execute). The next three presents the permission granted to a group of a file and the last three represetns the permissions that everyone else on the system as to this file. By the way, you can tell who is the owner of the file and then what group the file (```... dangnguyen dangnguyen ...```) belongs to by looking at this ```ls``` output.

-------------------------------------------------------------------------------------

### Shell Builtin Commands

> ```cat``` is short for *'concatenate'*

 which will then display the content of the file on the screen of the terminal.
```bash
cat day1.sh
```
returns
```bash
#!/bin/bash
echo "I dont have to be great to start, but I have to start to be great!"
```

> `#!`  is called *'shebang'*
> whereas `/bin/bash` indicates for what program will execute the following commands in the file, else it will use the current one in the shell.

*Note: It is very important since we don't know exactly what logged-in shell other people are using, and that may cause errors if they try to execute our script*


> `.` means the current directory of the working space
> `..` means the parent directory (one before the current)
> `pwd` is short for *'present working directory'*
```bash
dangnguyen@DangNguyenLap:~$ cd .
dangnguyen@DangNguyenLap:~$ pwd
/home/dangnguyen
dangnguyen@DangNguyenLap:~$ cd ..
dangnguyen@DangNguyenLap:/home$ pwd
/home
```
Therefore `./day1.sh` is running the script file in the current directory. Let say if we are in `/home` directory, the command for running `day1.sh` would be 
```bash
./dangnguyen/day1.sh
```
equivalent to
```bash
/home/dangnguyen/day1.sh
```
Another built-in command we need to look into is the `echo` command
```bash
dangnguyen@DangNguyenLap:/home$ type echo
echo is a shell builtin
dangnguyen@DangNguyenLap:/home$ type -a echo
echo is a shell builtin
echo is /usr/bin/echo
echo is /bin/echo
dangnguyen@DangNguyenLap:/home$ /usr/bin/echo "Hello world"
Hello world
```
Now we create a different script file called `day2.sh`
```bash
#!/bin/bash
SKILL="shell scripting"
echo "I want to be good at ${SKILL}. That's why I practice ${SKILL}."
```
>`SKILL` is the variable that we assigned. Note that, there must not be any space between the variable and the equal sign.

-------------------------------------------------------------------------------------
### Variables, Comments, and capitalization


-------------------------------------------------------------------------------------
### Writing long and complicated scripts




