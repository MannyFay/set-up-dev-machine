In this article I set up a Macintosh computer for web development.  
If there something is not working, please let me know.

## Recommendation
Choose a Mac with a minimum of 16 GB RAM and 1 TB disk space.
I'm on a MacBook Air M1 (so called Apple silicon) with macOS Ventura.
As keyboard layout I recommend an ANSI US layout.

## Set Up
In this part I start from srcatch with a new Mac (or an clean installation of macOS)
* Unbox your Mac and plug it into the power source
* Press the power button and hold it down till your Mac says, that you can leave the button
* Choose `Options`
* Choose `Disk Utility`

### Disk Partitions
By default your Mac comes with one big APFS partition for the whole system.  
That's good for the performance of macOS, but not so well for development. So you need two partitions in total.
The problem for development is, that the default APFS partition is case-insensitive.  
What means that?  
Imagine you have a directory (folder) called `Coding`. In this directory exists a file `my-documentation.md`. Fine, but if you try to create
a second file named `My-documentation.md` your Mac don't creates it because it says 'Hey, I have allready a file called `my-documentation.md`'.
So `my-documentation.md` and `My-documentation.md` is the same file for your Mac. That's what case-insensitivity is.  

In web development you work with a lot of Linux computers (servers, machines of colliques) and you maybe create some web applications that 
have a interface to change things by users. There comes the problem. Linux is case-sensitive. So `my-documentation.md` is a completely other
file than `My-documentation.md`.

### First Partition
Here runs macOS. Choose the disk `Macintosh HD` and give it 200 GB of space, so it has enough space to breathe for all your apps and system stuff.  
Select `APFS`. Now worries, it will be encrypted later.

### Second Partition
Here is the place for all your stuff. Create a partition and name it `Users`. That's important because with this name your apps don't will run 
into problems. Give it the space of all the rest of your disk and select `APFS (case-sensitive)`.  
You are ready to go! Press `Apply`.

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
