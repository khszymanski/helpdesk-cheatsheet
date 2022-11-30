# helpdesk-cheatsheet
---
## Windows 10
### Every commands work in powershell, run as administrator

**- Get Windows Product Key**

`wmic path SoftwareLicensingService get OA3xOriginalProductKey`

**- Change hostname**

`Rename-Computer -NewName "New hostname"`

**- Join a pc to doman**

`Add-Computer -DomainName DomainName -Restart`

**- Reboot/shutdown pc**

`shutdown -r -t 0 /f` 

`shutdown -s -t 0 /f`

`-r` -> reboot, `-s` -> shutdown
`-t 0` -> time (sec) to shutdown 
`/f` -> force

**- Restart spooler/printer service**

`net stop spooler`
then
`net start spooler`


## Windows 10 tools

---

## PROXMOX
### CLI

**1. Reboot proxmox**
`shutdown -r now`
