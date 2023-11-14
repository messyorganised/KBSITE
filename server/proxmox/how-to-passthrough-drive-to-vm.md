---
description: This article will guide you how passthrough hard drives straight to your VM.
---

# How to Passthrough drive to VM

Doing this will allow you to dual boot directly to your drive in case there is an issue with your Proxmox server. This is great especially if you're setting up PFSense as a VM as it allows us to reboot our machine straight into PFSense if Proxmox stopped working.



To begin drive passthrough, we need to understand why we are doing things the way we do in this guide. The reason why we passthrough drive by using the drive ID is because the ticker assigned by Proxmox to our drive's changes frequently.&#x20;



Terminology:

Using the drive ID to map our drive is like having the mailman send the mail to your house instead of physically handing the mail to you directly. Your house address does not change but you are mobile and can move around from one place to another.

## Locate your drive ID.

Access your shell and enter the following command.

```
ls -n /dev/disk/by-id/
```

This will give you a list of all drive connected to your hardware by its ID. Take not of the drive that you would like to pass through to your VM.&#x20;

For the sake of this tutorial, we will call our drive ID = DISK-ID



## Set your Drive ID to the desired VM.

Once you have acquired the DISK-ID enter the following string of command. Keep note of the following:

VM-ID = Your VM ID assigned by proxmox.

DISK-ID = The drive ID you would like to pass through to your VM.



Modify your command as per your configuration and remove the bracket \[]&#x20;

```
/sbin/qm set [VM-ID] -virtio2 /dev/disk/by-id/[DISK-ID]
```

## Final

Once you have completed the following. Your hard disk should be visible under your VM configuration page. This will allow you to boot into the machine via VM and Bare Metal.
