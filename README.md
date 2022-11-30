# helpdesk-cheatsheet
---
## Windows 10
### Every commands work in powershell, run as administrator

**1. Get Windows Product Key**

`wmic path SoftwareLicensingService get OA3xOriginalProductKey`

**2. Change hostname**

`Rename-Computer -NewName "New hostname"`

**3. Join a pc to doman**

`Add-Computer -DomainName DomainName -Restart`

**4. Reboot/shutdown pc**

`shutdown -r -t 0 /f` 

`shutdown -s -t 0 /f`

`-r` -> reboot, `-s` -> shutdown
`-t 0` -> time (sec) to shutdown 
`/f` -> force

---

## PROXMOX
### CLI

**1. Reboot proxmox**
`shutdown -r now`
