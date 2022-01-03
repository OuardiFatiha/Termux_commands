# Termux_commands
Termux is an Android terminal emulator and Linux environment Android app that works directly with root and without root. <br>
A Terminal base system is installed automatically – additional packages are available using the APT package manager.
## Storage setup, Update and Upgrade Command

- `termux-setup-storage`
- `apt-update`
- `apt upgrade`

## Apt Command
 `apt` is a command-line utility for installing, updating, removing, and otherwise managing deb packages on Ubuntu, Debian, and related Linux distributions. It combines the most frequently used commands from the `apt-get` and `apt-cache` tools with different default values of some options.
 `apt` is designed for interactive use. Prefer using `apt-get` and `apt-cache` in your shell scripts as they are backward compatible between the different versions and have more options and features.
 Most of the `apt` commands must be run as a user with `sudo` privileges.
- Listing all packages: `apt list`
- Installing a package: `apt install` or `pkg install`
  ex: `pkg install zile`,
      `apt install cmatrix`.
  checkout if they have been installed in the list of packages.
  running cmatrix like in the Matrix movie: `cmatrix`
  ![](cmatrix.jpeg)
  
  - Updating package index (`apt update`)
  - Upgrading packages (`apt upgrade`)
  - Full Upgrading (`apt full-upgrade`)
  The difference between upgrade and full-upgrade is that the later will remove the installed packages if that is needed to upgrade the whole system.
  - Installing packages (`apt install`)
  - Removing Packages (`apt remove`) : apt remove package-name
  - Remove Unused Packages (`apt autoremove`)
  - Searching Packages (`apt search`)
  - Package Information (`apt show`)
  
  Knowing how to manage packages is an essential part of Linux system administration.
 `apt` is a package manager for debian based distributions. To learn more about the `apt` command open your terminal and type `man apt`.
 
 
 ## Package Management Systems
 Most package systems are built around collections of package files. A package file is usually an archive which contains compiled binaries and other resources making up the software, along with installation scripts. Packages also contain valuable metadata, including their dependencies, a list of other packages required to install and run them.
 
|   Operating   | SystemFormat  |      Tools                    |
| ------------- | ------------- | ----------------------------- |
| Debian        | .deb          | apt(apt-cache, apt-get, dpkg) |
| Ubuntu        | .deb          | apt(apt-cache, apt-get, dpkg) |
| CentOS        | .rpm          | yum                           |
| Fedora        | .rpm          | dnf                           |
| FreeBSD       | .txz          | make,pkg                      |

## Update Package Lists
Most systems keep a local database of the packages available from remote repositories. It’s best to update this database before installing or upgrading packages. As a partial exception to this pattern, yum and dnf will check for updates before performing some operations, but you can ask them at any time whether updates are available.

|    System     |    Command          |    
| ------------- | ------------------- |  
| Debian        | sudo apt-get update |
| Ubuntu        | sudo apt-get update |
| CentOS        | yum check-update    | 
| Fedora        | dnf check-update    | 
| FreeBSD       | sudo pkg update     |

## Termux Basic Commands
| Command  | Usage  | Example  | Explanation  |   
|---|---|---|---|
| clear  | `clear`  | `clear`  | Clear Screen  |   
| pwd  | `pwd`  | `pwd`  | Current Working Directory  |   
| cd  | `cd`  | `cd /home`  | Changing Directory  | 
| touch  | `touch <file-name>`  | `touch file.txt`  | Create New File  |
| mkdir  | `mkdir <new-directoy-name>`  | `mkdir new_folder`  | Create New Directory  |
| rmdir   | `rmdir <directory-name>`  | `rmdir new_folder`  | Delete Directory  |
| rm   | `rm <file-name>`  | `rm file.txt`  | Delete File  |
| mv   | `mv <old-filename> <new-overwirte-filename>`  | `mv old_file.txt new_file.txt`  | Rename File and Directory & Move a File  |
| cp   | `cp <filename> <new-filename>`  | `cp file.txt new_file.txt`  | Copy File and Directory  |
| vi   | `vi <filename>`  | `vi file.txt`  | File Editor VI  |
| nano   | `nano <filename>`  | `nano file.txt`  | File Editor nano  |
| cat   | `cat <filename>`  | `cat file.txt`  | Read File Content  |
| top   | `top`  | `top`  | All running background Process Top command  |
| chmod   | `chmod (permission-mode) <filename>`  | `chmod +x file.sh`  | Change Permission  |
| chown   | `chown (newuser:newgroup) <filename>`  | `chown new_user file.txt`  | Change Group  |
| git clone   | `git clone <cloning url>`  | `git clone url`  | Clone Source code from Github  |
| wget   | `wget <download-file-url>`  | `wget url`  | Download File wget  |
| curl   | `curl <download-file-url> -o <output-filename>`  | `curl url -o out.pdf`  | Download File curl  |
| history   | `history`  | `history`  |  All Previous run Command  |
