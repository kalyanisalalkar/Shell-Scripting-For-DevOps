How to Create a Shell Script in linux using EC2 Instance
Shell is an interface of the operating system. It accepts commands from users and interprets them to the operating system.
Creating a Shell Script
You need to log in to your AWS account, create an EC2 instance and connect to it over ssh. Open the terminal and connect to the instance over ssh using the following command. 
sudo ssh "   "
Shell scripts end with the extension ".sh".
vim script.sh
Now, this script file is not executable by default, we have to give the executable permission to this file. Type in
chmod 754 script.sh
Now, we will add some commands to this shell script. Open this shell script with any text editor of your choice (command-line based or GUI based) and add some commands. We will use vim. Type in 
vim script.sh
Defining the Shell Script interpreter
There are many Shells available in Linux, such as The bourne shell(sh), The Korn Shell(ksh), and GNU Bourne-Again Shell(bash). Scripts written for the sh shell are called shell scripts, and they can be interpreted by both, the ksh and bash shells.Bash is generally the default shell in most of the Linux Distributions and scripts written specifically for bash shell are called bash scripts. 
You can specify which shell the script will use, even if the script is executed from another shell terminal. To do this, add “#!” on top of the script file, followed by the absolute path of the shell of choice. To specify bash as an interpreter, Add the following line on top of the shell script.
#!/bin/bash
This line is called the shebang line.
Note: This will only work if bash is installed on your system. 
#!/bin/bash
echo "This is my first shell script"
touch test.txt
ls
echo "End of my shell script"

run the shell script by typing in
./script.sh
