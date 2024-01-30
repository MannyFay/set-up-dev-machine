# Set Up Ubuntu Linux on a Real Machine
After you have followed [this steps](/docs/ubuntu.md) you can start with the installation of Ubuntu.

You need to create a bootable USB stick. For that I use [balenaEtcher](https://www.balena.io/etcher/).  
Now you can boot from the USB stick and install Ubuntu.

<br>

I choose the following settings:
* Minimal installation
* Download updates while installing Ubuntu
* Install third-party software for graphics and Wi-Fi hardware and additional media formats
* Erase disk and install Ubuntu (with disk encryption)

<br>

After the installation you have to reboot your machine and log in with your user.  
Wait a moment till the system is ready.
* Don't send anonymous system usage data to Canonical
* Don't use location services
* Install the updates the upcoming dialog asks you for
* Reboot your machine

<br>

Open a terminal, then...  
Turn off sending system information to Canonical:
```shell
ubuntu-report -f send no
```
Turn off package popularity contest:
```shell
sudo apt remove popularity-contest
```
Turn off automatic bug reporting:
```shell
Settings > Privacy > Problem Reporting > Off
```
Reboot your machine from terminal:
```shell
reboot
```

<br>

For the rest of the installation process I use my [Ansible Playbook](https://github.com/MannyFay/ansible).

