# Prepare VMware Workstation
## Windows as Host System
There are some things you can boost up the performance of VMware Workstation.

Open Command Prompt as administrator:
```bash
bcdedit /set hypervisorlaunchtype off
# To set it on again if needed:
bcdedit /set hypervisorlaunchtype auto
```
Disable memory integrity (in GUI):
```shell
Windows Security > Device Security > Core Isolation details
```
PowerShell:
```bash
powercfg /powerthrottling disable /path 'C:\Program Files (x86)\VMware\VMware Workstation\vmware.exe'
```
Reboot machine.

