                                                                                              
<div align="center">

<img src="./Assets/logo.gif" width="40%" />
</div>

## Description

This utility aims to help users quickly setup full-disk encryption, with the intent of providing a basic encryption setup for the user.

## Pre-Setup

You <b>cannot</b> encrypt your system while it's in use. You must boot into another system to run this script.
A good choice is to burn a clonezilla iso to a USB drive. Clonezilla has all the software that we need to setup encryption on the main drive.

### Required Packages
There are two required packages: initramfs-tools, and cryptsetup.

Both are available in the default Ubuntu repositories. And it is assumed that most Ubuntu derivatives will also carry these packages.

    sudo apt update
    sudo apt install cryptsetup initramfs-tools

### Get a Live-CD

Download the Clonezilla ISO
      
<a href="https://mirrors.xtom.com/osdn//clonezilla/71030/clonezilla-live-2.6.1-25-amd64.iso">clonezilla-live-2.6.1-25</a>

If you need an image writer you can <a href="http://wiki.rosalab.ru/ru/images/2/24/RosaImageWriter-2.6.1-lin-x86_64.txz">Download</a> RosaImageWriter.

### Backup System

### Partition Layout

### Tested Distributions
put these in tables
Ubuntu 18.04 EFI and DOS 
Zorin OS 15 EFI and DOS

## Limitations

Not compatiable with lvm - notes
Check to see if other non-ubuntu distros work

## Security Concerns



## Download

    curl --location 'https://tinyurl.com/yxekdxwq' > encrypt.sh && chmod 744 encrypt.sh

## Running The Script

Example output for an operation
Explanation of questions the script asks the user.

### Manually Configuring

  All configuration options that are actually run when the script runs\

#### General Configuration

#### Specific for EFI

#### Specific for i386

## Post Execution
reboot system 
recovery options
 - restore from backup (easiest)
 - cryptsetup-reencrypt /dev/partition_of_root --decrypt (will have to reconfigure the system. Cannot be undone!)
 - if both fail acknowledge i take no responsibility for damages

#Reminders to write about:
#State that this tool (for the moment) only is used to 'stapple' encryption onto the drive. Explain the security risks in doing so #and provide alternative methods for acheiving a safer setup.
#Add efi support and signing uefi keys.
#See if it is possible to create an auto-updater, and an option or separate script that embedds and updates the main script in a clonezilla image.
