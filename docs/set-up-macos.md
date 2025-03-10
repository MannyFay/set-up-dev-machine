# Set Up Dev Device - Native Apple macOS

## Set Up - Clean Installation of macOS

* Unbox device
* Plug it into a power source
* Press the power button and hold it down till your Mac says `Loading start up options`
* Choose `Options`
* Choose Language - English
* Choose `Disk Utility`

### Disk Partitions
Macs ship with one big 'APFS' partition for the whole system (improves performance of the OS, is not case-sensitive).

#### Partition 1 - System
* Size: 250 GB
* Select `APFS` (encryption setup will be done later)

#### Partition 2 - User
* Size: Rest of the disk
* Select `Volumes > +`
* Name: `Users` (important to name it `Users` because some apps need this name)
* Select `APFS (case-sensitive)`
* Press `Apply`.


* Close `Disk Utility`
* Run macOS
* Open `Finder` > `Settings` > `Sidebar` > Mark `Hard disks`
* Copy all directories in `Macintosh HD/Users` to your second partition into `Users`
* Open `System Settings` > `Users & Groups` > `Right click on your user` > `Advanced Options` > Set Home directory to `/Volumes/Users/yourUserName`

Your home directory is now setted on the case-sensitive partition so you can start with your development projects.. to be continued...

# WIP documentation
Install Nerd-Font:
```shell
brew tap homebrew/cask-fonts &&
brew install --cask font-space-mono-nerd-font
```
