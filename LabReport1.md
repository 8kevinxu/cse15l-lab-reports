# Week 1 Lab Report

## How to log into a course-specific account on ieng6 (Remotely Connecting)
### Step 1: Download Visual Studio Code (if you don't already have it)
Go to [(https://code.visualstudio.com/)](https://code.visualstudio.com/), and follow the instructions to download and install it on your computer. Download the version that corresponds to your computer, i.e. if you have a mac, install the mac version, otherwise you'll run into problems. When it is installed, it should open a window that looks like this when opened.
![Image](VSCODE.png)

### Step 2: Connect Remotely
Open the terminal on Visual Studio Code and use the ssh command along with your course specifc-account. Look up your course-specific account here: [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php) You'll have to set your password and wait a couple minutes.

This is what the command you're typing in should look like. 
```
$ ssh cs15lwi23zz@ieng6.ucsd.edu
```

Since it was my first time connecting to the server, I got a message like this:
```
⤇ ssh cs15lwi23zz@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```

I typed yes and pressed enter, and then typed in my password; the interaction should look like this (for my computer specifically, the password doesn't come up as you type it, you may run into the same problem but don't worry because the client still receives the password)

```
# On your client
⤇ ssh cs15lwi23zz@ieng6.ucsd.edu
The authenticity of host 'ieng6-202.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
Password: 
```

My terminal looked like this once I logged in.
![Image](remoteconnect.png)


### Step 3: Running Some Commands
I tried running commands I learned about in class like ls, pwd, and cd on my computer as well as the remote computer. 
  
Here is an example of me executing some of the common commands:
![Image](runningcommands.png)

I was able to figure out and get more comfortable with the commands just by trying different commands out. For example, I figured out what ls -lat does by simply typing it into the terminal, and saw that it posted directories with dates and times, which tells me that the command ls -lat lists directories/files by date. 



