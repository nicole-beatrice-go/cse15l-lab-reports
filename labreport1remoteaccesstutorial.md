# Lab Report 1: Remote Access and FileSystem Tutorial
Welcome to all incoming CSE15L students or my future self! Yay! :D

This will be a tutorial on how to log into an account on `ieng6`. Such fun!

This means that you'll be able to connect to a computer in the CSE basement and run commands through it.

This tutorial will be split up into 3 parts:
1. Installing VS Code

* This is the code editor that you will use and run commands on within its terminal
2. Remotely Connecting

* This is where you connect to a computer in the CSE basement
3. Trying Commands


* This is where you can run commands (can be on your own computer or the remote computer you're connected to) to navigate the FileSystem

---
## Installing VS Code
VS Code will be the code editor that you will use to code and run commands in its terminal. The first step is to install it.
> FYI: VS Code stands for Visual Studio Code!

The version you install depends on what operating system you have, which depends on what device you're using like Mac or a PC (macOS or Windows respectively).

This is the Visual Studio Code Website: [VS Website](https://code.visualstudio.com/). It has instructions on how to install VS Code and let's go through it together.

1. Download VS Code

If you have a Mac, download the macOS version. If you have a PC, download the Windows version. The screen to download should look like this. 

![Image](Screen%20Shot%202023-04-09%20at%204.11.09%20PM.png)

If you have Windows, you simply just need to run the installer. Then, VS Code should be under `C:\Users\{Username}\AppData\Local\Programs\Microsoft VS Code`.

However, there are a couple more steps for Mac. 


2. Find the app in Finder.

Click on the browser download at the bottom of your screen. Then, you will see it in **Finder**.

If it is archived in a zip, simply double click on the zip to extract its contents. 

![Image](Screen%20Shot%202023-04-09%20at%204.16.29%20PM.png)

![Image](Screen%20Shot%202023-04-09%20at%204.18.40%20PM.png)


3. Drag the app file to your **Applications** folder

Hold down on the app file `Visual Studio Code.app` in your **Downloads** and drag it to the left toward your directory to drop it into your **Applications** folder. 

By doing this, VS Code will become visible on your **Launchpad**.

![Image](Screen%20Shot%202023-04-09%20at%204.26.03 PM.png)


4. Open VS Code

You can open VS Code by double clicking on its app icon in your **Applications** folder.

However, if you want to add VS Code to your Dock you can right-click on the icon (which will temperarily be in the Dock while opened) and choose **Options**, then **Keep in Dock**.

![Image](Screen%20Shot%202023-04-09%20at%204.28.01%20PM.png)

![Image](Screen%20Shot%202023-04-09%20at%204.30.24%20PM.png)


This is what VS Code should look like once you open it. 
![Image](Screen%20Shot%202023-04-09%20at%205.47.26%20PM.png)


Congrats! Now you have VS Code installed and can follow your coding dreams! Now on to the next step and connecting to a remote computer!

---
## Remotely Connecting
Next, you will connect to a remote computer in the CSE basement. First, make sure that you have a CSE15L account using the account-lookup website:

[CSE Account Lookuo](https://sdacs.ucsd.edu/~icc/index.php)

You can then reset your login info and password with these instructions.

[Reset Password](https://drive.google.com/file/d/17IDZn8Qq7Q0RkYMxdiIR0o6HJ3B5YqSW/view?usp=share_link)


> FYI: Why is connecting to a remote server important?
> 
> You will often have a designated account for CSE or for your future job, which will give you access to a remote computer. This is important because by connecting to a remote computer through the Internet, you can access its files and work on it. This will help you accomplsh your job and collaborate with coworkers (even if they're far away)! 

Here are the steps!

1. If you have Windows, install `git` for Windows

Git has useful tools we need for VS Code! You can use the following link to install it: [Git](https://gitforwindows.org/)

Simply press the download button!


2. Open a terminal in VS Code

To do this, you can be on your VS Code window and go to the top to click Terminal, then New Terminal. You can also do a keyboard shortcut by doing `Ctrl + backtick`.


3. Set your default terminal to `git bash` in VS Code

First, you must open the command palette by either pressing the search bar at the top or doing `Ctrl + Shift + P`. Then, type in "Select Default Profile" and select that.

![Image](Screen%20Shot%202023-04-09%20at%205.02.50%20PM.png)

Then, select Git Bash.

![Image](Screen%20Shot%202023-04-09%20at%205.03.06%20PM.png)

Make sure that it is bash by looking at the + icon on the top right of your terminal.

![Image](Screen%20Shot%202023-04-09%20at%205.32.22%20PM.png)


4. In the terminal, write the following command except the "zz" is replaced by the last 2 characters of your CSE15L account:

`$ ssh cs15lsp23zz@ieng6.ucsd.edu`

> FYI: Don't type $, it's just convention to indicate that this is a command

5. Respond `yes` once you get this message

```
⤇ ssh cs15lsp23zz@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```

> FYI: It's okay to say yes because it's a new server. But if you get this message to a server you go to a lot, then someone might be trying to get to your connection to the server.

6. Enter your password for your CSE15L account

> FYI: Your password won't show as you type it but it still works. 

You should have a terminal that looks something like this afterwards

![Image](Screen%20Shot%202023-04-09%20at%205.48.02%20PM.png)

This means that you're now connected to your remote computer! Yay! Now you can run commands!

> FYI: The computer you are currently on is the *client* while the remote computer you are conected to in the CSE basement is the *server*.
---
## Trying Commands
Finally, you can run some commands!

Here's a brief rundown of what each command does:

* `cat <path1><path2>` : (means concatenate) prints out the contents of the files within the given paths
* `ls <path>` : (means list) lists the files and folders of the path
* `pwd` : (means print working directory) prints the current working directory and the abolsute path to get to it
* `cd <path>` : (means change directory) switches from the current working directory to another given path

> FYI: Paths describe wher a file is on a computer like which folders you have to go through to get there. Absolute paths are the whole path while relative paths don't include the root.
> FYI: The directory is the top of the path as it's a folder that's not contained in any other folder. 

Go ahead and try any combo of these commands using different paths on your remote server by typing them in the terminal!

Here's an example:

![Image](Screen%20Shot%202023-04-09%20at%206.13.28 PM.png)

Finally, to log out of the remote server, you can do the following:
1. `Ctrl + D`
2. Run command `exit` by simply typing "exit" and pressing Enter

---

That's all for the tutorial! I hope this was helpful and that it was fun! Thank you so much and have a good one!


