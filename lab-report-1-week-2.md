# Week 2 Lab Report: Tutorial for Remote Access
## By Jerry Gong
> **Part 1: Installing Visual Studio Code**

* Go to the [Visual Studio Code website](https://code.visualstudio.com/), then follow the instructions to download and install.
* Once you complete, you should be able to open VScode with a window like this:

  ![image](part1.png)
 
 > **Part 2: Remotely Connecting**

* If you're on Windows, go to [Install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) and install this program called OpenSSH which is capable of connect your computer to other computers.
* Then, look up your own account for CSE15L by going to [account lookup](https://sdacs.ucsd.edu/~icc/index.php).
* At first, open a terminal in VSCode (Click Terminal and choose New Terminal on menu option). Enter a command like this, but with your own course-specific account.

    `$ ssh cs15lwi22jjj@ieng6.ucsd.edu`
* If this is your first time logging in, you may get a message like this:

    `The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
    RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
    Are you sure you want to continue connecting (yes/no/[fingerprint])?`
* Say yes to this message and give password to continue logging in.
* When you successful log in, your terminal should look something like this:

    ![image](part2.png)

> **Part 3: Trying Some Commands**

* Commands can be ran both on your computer and on the remote computer after ssh-ing. Below are some useful commands to try out!

    `cd ~` - Change directory.
    
    `ls` - Lists all files in the current directory except for hidden files.
    
    `ls -a` - Lists all files including hidden files(files with names beginning with a dot).
    
    `ls -l` - Gives a long listing of all files.
    
    `ls -t` - Lists the files in order of the time when they were last modified.
    
    `cp ~` - Copies files or group of files or directory.
