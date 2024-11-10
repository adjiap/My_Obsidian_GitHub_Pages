---
created on: 2024-06-16
last modified on: 2024-06-16 19:32:08
aliases: 
tags:
  - linux
  - powershell
  - codesnippet
  - wsl
---

---
# Setup on Windows
## Enabling WSL
%% $^3$ $^4$ %%
```powershell
# As Admin
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

# If you want to know which are installed
# dism.exe /online /Get-Features
```
## WSL install Ubuntu
%% $^1$ %%
```powershell
# To check which distro exists, use the following
# `wsl -l --online`

# By default, it will install Ubuntu's latest version, otherwise
# `wsl -i -d Ubuntu`
wsl --install

# Open the wsl for Ubuntu
wsl -d Ubuntu
# Then create username and password if it doesn't exist yet
```

## WSL Install a 2nd Ubuntu
%% $^5$ %%
> [!info]
> This might be useful, if you want to have a separate workstation for something else

```powershell
# Export the WSL that you want to base things of
wsl --export Ubuntu .\temp_ubuntubackup.tar

# Create the second Ubuntu (name is case-sensitive)
wsl --import Ubuntu-2 "C:\Users\MyName\This\Is\Install\Folder" .\temp_ubuntubackup.tar

# Enter the second Ubuntu
wsl -d Ubuntu-2
```
### Find the Distros installed in WSL
%% $^6$ %%
```powershell
Get-ChildItem "HKCU:\Software\Microsoft\Windows\CurrentVersion\Lxss" -Recurse
```
### Fix issue regarding default user
```powershell
# Problem mentioned in https://github.com/microsoft/WSL/issues/4276, where the imported distro puts you in `root`

# We need to create an extra /etc/wsl.conf
sudo nano /etc/wsl.conf
# Input the following:
# 
# [user]
# default=<default_username>

# Exit the Ubuntu-2 environment
exit

# And terminate the environment for virtual reboot
wsl --terminate Ubuntu-2

# Enter the WSL environment again with the default user changed.
wsl -d Ubuntu-2
```

## WSL remove environment
```powershell
# This will remove the installed WSL environment of the kali-linux distro 
wsl --unregister kali-linux
```
# Prep virtual Linux with remote desktop GUI
%% $^1$ %%
```sh
# Update distro
sudo apt update

# Install GUI to RDP from Windows
sudo apt install xfce4 xrdp dbus-x11 -y

# Start RDP session
sudo /etc/init.d/xrdp start

# Get IP Address of RDP session
ifconfig

# Then RDP into the Linux session using the IP address
```

# Adding Directory to a Path to Linux
%% $^2$ %%
## Temporarily
```sh
export PATH="/Directory1:$PATH"
```
## Permanently
Firstly, open the `.bashrc` (current user) or `.profile` (for all users), then enter the following, at *the end of the file*
```txt
export PATH="/Directory1:$PATH"
```

Save and execute the script, or reboot the system
# Other linux code snippet files
```dataview
TABLE
FROM "01_Atomic_Notes" AND (#linux AND #codesnippet)
```


---
 $^1$ [Kali Linux: WSL 2 install and GUI setup (youtube.com)](https://www.youtube.com/watch?v=oTD8cYluUgk&list=PLhfrWIlLOoKNMHhB39bh3XBpoLxV3f0V9&index=5&ab_channel=DavidBombal)
 $^2$ [Linux: Add a Directory to PATH {Temporarily or Permanently} (phoenixnap.com)](https://phoenixnap.com/kb/linux-add-to-path)
  $^3$ https://learn.microsoft.com/en-us/windows/wsl/install-manual
 
 $^4$ https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/enable-or-disable-windows-features-using-dism?view=windows-11
 
 $^5$ https://learn.microsoft.com/en-us/windows/wsl/basic-commands
 
 $^6$ https://askubuntu.com/a/1380274

