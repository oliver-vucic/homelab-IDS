# Architecture

## Physical and virtual platform

**Host Hardware:**

The device that hosts the Proxmox VE is a HP EliteDesk 800 G3 Mini. The hardware specifications are:
- 16 GB RAM
- i5-7500 4-core
- single NIC
- 256GB total device storage

This platform is more than capable at supporting the three VMs it hosts, because of the amount of RAM, the four cores and the sizeable storage.

<br/>

**Hypervisor Choice:** Proxmox VE was primarily chosen because it runs well on cheap hardware (i.e. it would run well on the mini pc) and it is a type 1 hypervisor that is free and open source, perfect for a home-lab. The native support for Linux bridges and containers was also a bonus.

<br/>

**Logical Volume Manager (LVM) Choice:** LVM-thin was chosen as it is the Proxmox default logical volume manager for a single disk. The thin provisioning and snapshot support met the lab's needs, so there was no change needed.

<br/>

**RAM Allocation:**
- **OPNsense** - it has 4GB of memory, which is the reasonable size that is recommended by [OPNsense]([url](https://docs.opnsense.org/manual/hardware.html)) to run all standard features.
- **Kali** - it has 4GB of memory, which is 2GB above [Kali's]([url](https://www.kali.org/docs/installation/hard-disk-install/)) minimum RAM requirements for a default Xfce4 desktop and kali-linux-default meta-package install. The extra 2GB of memory ensures that the VM runs smoothly.
- **Metasploitable 2** - it has 512MB of memory, which is the recommend RAM by [OffSec]([url](https://www.offsec.com/metasploit-unleashed/requirements/)).








