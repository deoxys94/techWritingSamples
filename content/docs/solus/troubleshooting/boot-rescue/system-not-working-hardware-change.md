---
title: "I changed hardware and now my system doesn't start"
icon: "sailing"
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
weight: 233
params:
  index: false
---

{{% alert context="info" %}}

- This is not the official documentation of Solus. If you need help with Solus, go to https://help.getsol.us/
- This documentation was originally created for the Solus Project, for which I was a contributor. The Solus Project is the sole rights holder of this work. See the [License page](/docs/license) for more information.

{{% /alert %}}

---

## Before your start

For this procedure, you need:

- A Solus live USB
- Your disk encryption password, if your system is encrypted

## Procedure

1. Shut down your system.
1. Boot from a Solus live USB.
1. Mount the partitions of your Solus system.
   
   <details>

      To recover your system, you need to mount the Solus root (`/`) partition and all other partitions your system uses.
      
      1. Open a terminal.
      1. Mount the Solus root partition:
      
         1. Access as the root user by using the following command:
      
            ```bash
            sudo su
            ```
      
         2. Create a directory to serve as the mount point for your Solus system:
      
            ```bash
            mkdir /target
            ```
      
         3. Find the drive and partition of your Solus system using the `lsblk` command.
      
            After running the command, the system displays a list of all the drives in your computer:
      
            ```
            NAME                  MAJ:MIN RM   SIZE RO TYPE MOUNTPOINT
            sda                     8:0    0 238.5G  0 disk
            ├─sda1                  8:1    0   512M  0 part
            ├─sda2                  8:2    0   234G  0 part
            └─sda3                  8:3    0     4G  0 part [SWAP]
            sdb                     8:16   0 465.8G  0 disk
            ├─sdb1                  8:17   0     1G  0 part
            └─sdb2                  8:18   0 464.8G  0 part
              ├─SolusSystem-root  253:0    0 234.3G  0 lvm
              ├─SolusSystem-swap  253:1    0   3.7G  0 lvm  [SWAP]
            sdc                     8:32   1  14.9G  0 disk
            ├─sdc1                  8:33   1   4.2G  0 part /cdrom
            └─sdc2                  8:34   1   4.1M  0 part
            nvme0n1               259:0    0 476.9G  0 disk
            ├─nvme0n1p1           259:1    0   500M  0 part
            ├─nvme0n1p2           259:2    0    16M  0 part
            ├─nvme0n1p3           259:3    0   475G  0 part
            └─nvme0n1p4           259:4    0   1.4G  0 part
            ```
      
            You can use drive size or the number of partitions in each drive to determine which one is your Solus drive.
      
	  		{{< alert context="info" text="If you installed Solus on a _SATA_ drive, the name of the drive might be `sdX` (For example, `sda`). If you installed Solus on an _NVMe_ drive, the name of the drive might be `nvme#n#` (For example `nvme0n1`)." />}}
      
            Write down the name of the drive and the type.
      
         4. If the type of your drive is **lvm** or if your drive is encrypted:
      
            1. Check if the drive is encrypted.
      
               Encrypted drives do not have the label **decrypted** after the drive name:
      
               ```bash
               sdb                     8:16   0 465.8G  0 disk
               ├─sdb1                  8:17   0     1G  0 part
               └─sdb2                  8:18   0 464.8G  0 part
                 ├─SolusSystem-root  253:0    0   100G  0 lvm
                 └─SolusSystem-swap  253:1    0     8G  0 lvm  [SWAP]
               ```
      
               Decrypted drives have the label **decrypted** after the drive name:
      
               ```bash
               sdb                     8:16     0 465.8G  0 disk
               ├─sdb1                  8:17     0     1G  0 part
               └─sdb2                  8:18     0 464.8G  0 part
                └─decrypted           253:1    0   238G  0 crypt
                   ├─SolusSystem-root  253:0    0 234.3G  0 lvm
                   └─SolusSystem-swap  253:1    0   3.7G  0 lvm  [SWAP]
               ```
      
            1. If your drive is encrypted, use `cryptsetup` to decrypt it.
      
               ```bash
               cryptsetup luksOpen /dev/partitionName decrypted
               ```
      
               For example
      
               ```bash
               cryptsetup luksOpen /dev/sdb2 decrypted
               ```
      
         1. Mount the Solus root partition:
      
            - If your drive's type is _lvm_
              ```bash
              mount /dev/mapper/SolusSystem-Root /target
              ```
            - Otherwise:
              ```bash
              mount /dev/sdX# /target
              ```
      
      1. If your computer uses UEFI, mount the EFI system partition:
      
         In new installations, the EFI system partition (also known as ESP) is usually 1 GB in size. For older installations, the partition is usually 512 MB in size.
      
         1. Use `fdisk` to check the partitions of your drive:
      
            - If you have a SATA drive:
              ```bash
              fdisk -o Device,Size,Type -l /dev/sdX
              ```
            - If you have an NVMe drive:
            
              ```bash
              fdisk -o Device,Size,Type -l /dev/nvme0nX
              ```
            
              The system displays something similar to this:
            
              ```bash
              Device       Size Type
              /dev/sda1    512M EFI System
              /dev/sda2  111.3G Linux filesystem
              ```
            
              In this case, the EFI system partition is `/dev/sda1`
      
      1. Mount the EFI system partition:
      
         ```bash
         mount /dev/sdX# /target/boot
         ```
      
         For example:
      
         ```bash
         mount /dev/sda1 /target/boot
         ```
      
      1. Mount other partitions your system might have (for example, `/home`):
      
         ```bash
         mount /dev/sdX# /target/home
         ```
      
      1. Chroot to your Solus system:
      
         Chroot allows you to execute commands and use utilities from your main system directly. This is necessary to do specific repairs like fixing the bootloader.
      
         1. Run the following commands:
            ```bash
            mount --types proc /proc /target/proc
            mount --rbind /dev /target/dev
            mount --rbind /sys /target/sys
            mount --make-rslave /target/dev
            mount --make-rslave /target/sys
            ```
         1. Chroot into your system:
            ```bash
            chroot /target
            ```
   </details>

1. Update the system configuration to address the hardware changes.
   <details>

   1. Re-run system-wide configuration triggers
      
      ```bash
      sudo usysconf run -f
      ```

   2. If you use an UEFI system, update the boot entries for your EFI menu: 

      ```bash
      sudo clr-boot-manager update
      ```
   </details>

1.  Unmount all the Solus partitions.

    <details>

       1. Exit the chroot environment by pressing <kbd>CTRL + D</kbd>
       2. Unmount the Solus partitions:

          ```bash
          umount -R /target
          ```

       3. If your drive is encrypted:
        
       	  1. Deactivate your logical volumes and volume groups:
          
       	     ```bash
       	     lvchange -a n /dev/SolusSystem/Swap
       	     lvchange -a n /dev/SolusSystem/Root
       	     vgchange -a n SolusSystem
       	     ```
          
       	  2. Close the LUKS partition:
          
       	     ```bash
       	     cryptsetup luksClose decrypted
       	     ```

    </details>

## What to do next

Restart your system and verify if the problem persists.

If you are still unable to access your Solus system after following this guide, contact us through any of the support channels.