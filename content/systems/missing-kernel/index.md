---
title: "No Kernel? No Problem! A Rescue Mission Told in CLI"
date: 2025-11-15
draft: false
description: "A Linux system recovery story told like an emergency room drama: complete with GRUB resuscitation, a kernel transplant, and a Kubuntu lifeline."
tags: ["linux", "arch", "grub", "btrfs", "recovery"]
---

```bash
error: file ‘/vmlinuz-linux-zen’ not found.  
Loading initial ramdisk…  
error: you need to load the kernel first.  
```

Were the grave words the GRUB spoke to me, the same way a paramedic informs a family member of the patient’s critical condition. In this story, however, there was no CPR or even any chest compressions… just a Live OS and some patience.

Initial instinct was to boot up an old GParted disk drive to chroot into the system. Only problem was that the install media hadn’t been updated in over twelve years, so both the Wi-Fi and graphics drivers failed in spectacular fashion. Still, it wasn’t time to give up on the case; even the `lsblk` and `fstab` showed signs of life.

After the sudden news, I went to the UEFI menu and got to my Windows partition, ready to create the recovery media through [Rufus](https://rufus.ie/en/) and a [Kubuntu ISO](https://kubuntu.org/download/).

Even if my NVIDIA setup caused the resolution size to be smaller than an 80’s flip phone, the objective was clear: getting that kernel back in place! Let’s head over to the Kubuntu terminal to make our first incisions.

---

The patient comes wheeling in on the stretcher as I mount my Btrfs drive:

```bash
kubuntu@kubuntu:~$ sudo mount -t btrfs -o subvolid=5,rw /dev/nvme0n1p2 /mnt
kubuntu@kubuntu:~$ sudo umount /mnt
kubuntu@kubuntu:~$ sudo mount -t btrfs -o subvol=@,rw /dev/nvme0n1p2 /mnt
```

Remember, if your drive’s blood type isn’t Btrfs, you can mount without the extra fuss. Remembering the [wisdom of Ted](https://unix.stackexchange.com/questions/91620/efi-variables-are-not-supported-on-this-system), we perform the blood transfusion to bind the directories:

```bash
kubuntu@kubuntu:~$ for i in /dev /dev/pts /proc /sys /sys/firmware/efi/efivars /run; do sudo mount -B $i /mnt$i; done
```

An electric shock followed by a mandatory `neofetch` reveals signs of life! We provide the pacman medication for the missing Linux kernel and then initiate a hard reset of his GRUB system:

```bash
kubuntu@kubuntu:~$ sudo chroot /mnt /bin/bash
[root@kubuntu /]# mount /dev/nvme0n1p1 /boot/efi
[root@kubuntu /]# ls /boot/efi/
EFI  'System Volume Information'  amd-ucode.img  dev  grub  proc  sys
[root@kubuntu /]# grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=GRUB
Installing for x86_64-efi platform.
Installation finished. No error reported.
[root@kubuntu /]# grub-mkconfig -o /boot/grub/grub.cfg
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-linux-zen
Found initrd image: /boot/amd-ucode.img /boot/initramfs-linux-zen.img
Found linux image: /boot/vmlinuz-linux
Found initrd image: /boot/amd-ucode.img /boot/initramfs-linux.img
Warning: os-prober will be executed to detect other bootable partitions.
Its output will be used to detect bootable binaries on them and create new boot entries.
Found Windows Boot Manager on /dev/nvme0n1p1@/EFI/Microsoft/Boot/bootmgfw.efi
Adding boot menu entry for UEFI Firmware Settings ...
done
```

The patient’s eyes bolt open. Thus, he is alive!

> “Wow, it feels like I just woke up from a bad headache… is there any rice in here?”

With his silly closing statement, I knew I had saved another patient here at the Linux Clinic.

—Dr. Adrian, 11/15/2025

