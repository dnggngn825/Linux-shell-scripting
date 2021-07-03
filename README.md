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

Then just type in the content in the script, hit ```Ctrl + X``` to save change and hit ```Y```
```bash
!#/bin/bash
echo "Hello World"
```
It will ask for filename, just press ```Enter``` and we will get our first script file. Now, to run the file
```bash
./day1.sh
```
which outputs
```bash
Hello World
```
