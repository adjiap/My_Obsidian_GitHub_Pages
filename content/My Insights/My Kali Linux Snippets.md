---
created on: 2024-06-16
last modified on: 2024-06-16 19:32:08
aliases: 
tags:
  - kalilinux
  - linux
  - powershell
  - wsl
  - codesnippet
---

---
# Setup on Virtual Box[^6]

> [!tip] Recommended!
> It is recommended that you use a virtual machine such as [Oracle VirtualBox](https://www.virtualbox.org/). This will have your actual home machine more protected and would leave any traces in the virtual box itself. Install on Windows using `winget install Oracle.VirtualBox`

## Download and implement Kali-Linux image
You can download the Kali-Linux image for virtual box [here](https://www.kali.org/get-kali/#kali-platforms) , extract the Zip file, and add it to the Virtual Box. Btw, the default user as well as password would be `kali`

![[images/Add_KaliLinux_to_VirtualBox.png]]

## Update Kali-Linux packages
It's likely that the Kali-Linux has outdated packages, and also, if you're behind a proxy, you would need to update the sources file, so do this
```sh
sudo nano /etc/apt/sources.list
# Then update the URL to use HTTPS (the first http, btw)
# so: `deb http://http.kali.org/kali...` -> `deb https://http.kali.org/kali...`
```

Then upgrade the basic kali packages
```sh
sudo apt update
sudo apt upgrade -y
```

# Setup [[Metasploitable 2]] [^7]
Download metasploitable in [SourceForge](https://sourceforge.net/projects/metasploitable/), and you can follow this tutorial from [freecodecamp](https://www.freecodecamp.org/news/how-to-set-up-metasploitable/) to install it.

> [!tip] Insight on 06.11.2024
> Most youtube videos regarding this setup, would be using Oracle Virtual Box 6. Starting from Oracle Virtual Box 7, it's much clearer to follow the instructions in freecodecamp

# Setup on Windows
## WSL install KaliLinux[^1]
%% $^1$ %%
```powershell
# To check which distro exists, use the following
# `wsl -l --online`

wsl --install kali-linux
wsl -d kali-linux

# Then create username and password if it doesn't exist yet
```

![[My Linux Snippets#Prep virtual Linux with remote desktop GUI]]

## Connect to Virtual Kali-Linux via native GUI ([Win-KeX](https://www.kali.org/docs/wsl/win-kex/)) [^2]

> [!warning]
> As of **28.10.2024** I have tried the direct login from Windows Terminal, and it doesn't work. If I am inside kali-linux WSL environment, and use `kex`, it works.

```sh
# Firstly update distro and install the newest Win-KeX
sudo apt update && sudo apt install -y kali-win-kex
```

> [!tip]
> If you don't really care that much about which mode you are using, just run this
> ```sh
> kex -s
> ```


```sh
# To close the client, you can just log out the GUI, and also shut it down using the following, with the <flag> being --win, --esm or --sl, respectively.
kex <flag> --stop
```
### Win-KeX Seamless Mode

```powershell
# Directly open from Windows Terminal
wsl -d kali-linux kex --sl -s
```

```sh
# In the kali-linux WSL
kex --sl -s
```
### Win-KeX Windowed Mode

> [!info] 
> Window Mode, is the **default** Win-KeX for Windows PC with Intel chips. It opens up a windowed application, which would help visually keep the two environments apart. Under the hood, it uses [TigerVNC](https://tigervnc.org/). More information, can be read in the documentation, [here](https://www.kali.org/docs/wsl/win-kex-win/)


```powershell
# Directly open from Windows Terminal
wsl -d kali-linux kex --win -s
```

```sh
# In the kali-linux WSL
kex --win -s
```
### Win-KeX Enhanced Session Mode

> [!tip]
> This is the only mode working for ARM devices!

> [!info] 
> ES Mode is the **default** Win-KeX for Windows PC with ARM chips. It will run in a separate window using protocols and clients native to windows. Under the hood, it uses [xrdp](https://www.xrdp.org/) servers, and Window's RDP connection. More information, can be read in the documentation, [here](https://www.kali.org/docs/wsl/win-kex-esm/)

> [!warning]
> The use of `--ip` is a temporary workaround due to a Windows bug that caused a massive packet loss when using localhost. If in the future it is fixed, we could remove it.


```powershell
# Directly open from Windows Terminal
wsl -d kali-linux kex --esm --ip -s
```

```sh
# In the kali-linux WSL
kex --esm --ip -s
```
# Kali Linux snippets

## Install Kali's default tools[^2]
```sh
sudo apt install -y kali-linux-large
```

> [!info] If you're currently learning OffSec...
> During installation of the default tools, it's likely you'd get `macchanger`, `kismet`, `wireshark`, `sslh` tool installation as well. My recommendation (just from feeling) is to install all, but not let wireshark to non-superusers, and do `from inetd` for sslh, 

## Install hash algorithm tool[^3]
```sh
sudo apt install hashrat
```

> [!info] If you're learning digital forensics
> This tool would be needed to create hash values to preserve evidence in forensic investigations

### Example usage
```sh
hashrat -sha1 "Linux Financial Case.001"| tr ' ' '\n'
# hash='sha1:c7b06f006ff79711e692bd2620aba4cc2a4426d2'
# type='file'
# mode='100777'
# uid='1000'
# gid='1000'
# size='1007681536'
# mtime='1486639076'
# inode='57420895249066205'
# path='Linux
# Financial
# Case.001'

# or
hashrat -sha1 "Linux Financial Case.001" -t
# c7b06f006ff79711e692bd2620aba4cc2a4426d2  Linux Financial Case.001
```

## Install hash decode tool
```sh
sudo apt install hashcat
```
## Install data carving/data recovery tool[^4]
```sh
sudo apt install foremost
```

```sh
hashcat
```
### Example usage
```sh
# Finding the foremost config file (also don't show me any errors)
find / -name foremost.conf 2>/dev/null
# /usr/local/etc/foremost.conf
# /etc/foremost

# Running foremost to recover images from the carved data
foremost -c foremost.conf -T -i '/home/sansforensics/Desktop/WinLabRaw.img'

# Recover only jpegs
foremost -c foremost.conf -t jpg -T -i '/home/sansforensics/Desktop/WinLabRaw.img'
```

## Create a file of a certain size[^5]
```sh
# Creates a file called "upload_test_1024k" with the size of 1024 Bytes, that is all zeroes
dd if=/dev/zero of=upload_test_1024k bs=1024 count=1
```
# Other kali linux snippet 
```dataview
TABLE
FROM "01_Atomic_Notes" AND (#kalilinux AND #codesnippet )
```

---
# See Also
[[My Linux Snippets]]

[^1]: [Kali Linux: WSL 2 install and GUI setup (youtube.com)](https://www.youtube.com/watch?v=oTD8cYluUgk&list=PLhfrWIlLOoKNMHhB39bh3XBpoLxV3f0V9&index=5&ab_channel=DavidBombal)
[^2]: [Win-KeX](https://www.kali.org/docs/wsl/win-kex/)
[^3]: [hashrat | Kali Linux Tools](https://www.kali.org/tools/hashrat/) 
[^4]: https://www.kali.org/tools/foremost/
[^5]: https://stackoverflow.com/questions/139261/how-to-create-a-file-with-a-given-size-in-linux
[^6]: [Setting Up Kali Linux & ColdBox on Oracle VirtualBox](https://www.youtube.com/watch?v=V5ywhofDgfA)
[^7]: [Linux Priviledge Escalation](https://www.youtube.com/watch?v=iiHAJc6AkxQ)
