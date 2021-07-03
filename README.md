# Linux-shell-scripting

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
### Create a first script
```bash
nano day1.sh
```
We can name the shell script anything and the script's end in ```.sh``` is not significant like it is in some other operating system

Then just type in the content in the script, hit ```Ctrl + X``` to save change and hit ```Y```
```bash
!#/bin/bash
echo "Hello World"
```
It will ask for filename, just press ```Enter``` and we will get our first script file. Now, to run the file, we first have to give it permission to run by using command ```chmod``` which means 'change mode', ```+x``` gives the file the execute permission
```bash
chmod +x day1.sh
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

