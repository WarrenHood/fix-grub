# Grub bootloader installer/reinstaller

## What is this?

Sometimes you need to dual-boot to play games on Windows. And sometimes Windows decides that you no longer need your linux bootloader.
This script can be placed on a flash drive or on an Arch live cd you build with Archiso. The idea is that you can simply rerun this script
whenever your bootloader gets deleted to quickly reinstall grub without trying to remember which partitions everything is on. 

Just edit the script once to set the partitions correctly, forget about it, and then rerun it whenever your bootloader gets deleted.
(Don't forget to update the script if your partitions change)

Before using this script, ensure that you are aware of what's what with your partitions.

You can list your partitions with `fdisk -l`.

Edit the `fix-grub` script's variables for your OS and EFI partitions accordingly.

## Warning

I haven't really tested this script. Next time my bootloader gets deleted by Windows I will update this README.

## Usage

Ensure that this script is executable with
```bash
chmod +x ./fix-grub
```

Then execute this script with
```bash
./fix-grub
```

It is assumed that your OS and EFI partitions aren't mounted, and that you execute this from an Arch live cd. 
The `arch-install-scripts` package should also be installed (it usually is) in your live iso.
