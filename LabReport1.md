# Week 1 Lab Report

## How to log into a course-specific account on ieng6
### Step 1: Download Visual Studio Code (if you don't already have it)
Go to https://code.visualstudio.com/, and follow the instructions to download and install it on your computer. When it is installed, it should open a window that looks like this when opened. 
![Image](VSCODE.png)

### Step 2: Connect Remotely
Next, open a terminal in VScode. (Ctrl or Command + `, or use the Terminal → New Terminal menu option). 
Your command should look like this (with the zz being replaced by the letters in your specific course account.:
```
$ ssh cs15lwi23zz@ieng6.ucsd.edu
```

If this is  the first time you’ve connected to this server, you will probably get a message like this:
```
⤇ ssh cs15lwi23zz@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```

Type yes and press enter, and then type in your password. 

You should have been logged on, and seen something like this. 

![Image](remoteconnect.png)

