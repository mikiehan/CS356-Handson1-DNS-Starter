# Juypter Notebook Setup

Choose Option 1 or Option 2 below.
After you are done with either Option 1 and Option 2, type below in your terminal 

    cd github-repo-root
    jupyter notebook & 
    
Open your browser and type
    
    localhost:8888

## Option 1: Install Juypter notebook 

You may install Jupyter notebook on your personal computer following [this instruction](https://jupyter.org/install).

## Option 2: Use UTCS machine

### Step 1: Install X Server 

#### macOS: 
Install [XQuartz](https://www.xquartz.org/). You will need to log out and log back in to complete the installation (as mentioned by the prompt at the end).

#### Windows 
Install [Xming](https://sourceforge.net/projects/xming/files/Xming/6.9.0.31/Xming-6-9-0-31-setup.exe/download). Use default options and uncheck "Launch Xming" at the end.

#### Linux

The X server is pre-installed!

Additionally, your personal computer's SSH terminal application must have X11 forwarding enabled:

In Linux, the SSH terminal supports X forwarding by default.
In macOS, you may need to edit your ssh_config file (typically found at /etc/ssh/ssh_config or ~/.ssh/config) if you have trouble using X forwarding. If ssh_config includes #X11Forwarding no (or just X11Forwarding no), uncomment out the line (remove the leading #), and change it to X11Forwarding yes.

In PuTTY for Windows, you can enable X forwarding in new or saved SSH sessions by selecting Enable X11 forwarding in the "PuTTY Configuration" window (Connection > SSH > X11).

### Step 2: ssh into UTCS machine with X forwarding

#### Linux or macOS:

0. If macOS, launch XQuartz server. 
1. Open your SSH terminal client.
2. On the command line, enter (replacing username and machinename):

        ssh -X username@machinename.cs.utexas.edu


#### Windows:
To use SSH with X forwarding in PuTTY for Windows:


### Step 3: Test if X forwarding is working
Try running xclock; on the command line, enter:

        xclock

If X forwarding is working, the xclock graphical clock will appear on your personal computer's desktop.
PuTTY for Windows

