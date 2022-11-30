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

**- Show ip address**

`ipconfig`

**- Allow/block ping**

enable ipv4

`netsh advfirewall firewall add rule name="ICMP Allow incoming V4 echo request" protocol=icmpv4:8,any dir=in action=allow`

enable ipv6

`netsh advfirewall firewall add rule name="ICMP Allow incoming V6 echo request" protocol=icmpv6:8,any dir=in action=allow`

disable ipv4

`netsh advfirewall firewall add rule name="ICMP Allow incoming V4 echo request" protocol=icmpv4:8,any dir=in action=block`

disable ipv6

`netsh advfirewall firewall add rule name="ICMP Allow incoming V6 echo request" protocol=icmpv6:8,any dir=in action=block`

all firewall frules

`netsh advfirewall firewall show rule name=all`


## Windows 10 tools
### Press Win+R and type:

**- Computer management**

`compmgmt.msc`

---

## PROXMOX
### CLI

**1. Reboot proxmox**
`shutdown -r now`
