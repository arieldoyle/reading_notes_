# Class 11 Reading Notes

## Data Restoration, Startup Repair, and Secure Disposal

### Resources

[SolarwindsMSP: SSD Data Recovery Best Practices](https://www.solarwindsmsp.com/blog/ssd-data-recovery-best-practices)
[How to Erase a Hard Drive Using DBAN](https://www.lifewire.com/how-to-erase-a-hard-drive-using-dban-2619148)

### SSD Data Recovery Best Practices

#### How do I know if my SSD is failing?

SSD failures are hard to detect since they do not emit audible signals

- Most common Indicators that the SSD is approaching its read/write cycle limit/experiencing physical issues:
  - Bad Blocks: storage segments that, through memory corruption or physical damage, impede data storage and retrieval functions
    - Symptoms:
      - Saving, reading, and moving files may result in failure
      - Active applications may operate slowly or frequently crash
      - User may receive prompts to repair the file system
      - General performance may steadily decrease, especially when handling large files.
    - Best Course of Action:
      - Run software that searches for physical defects. If the software discovers physical damage, you’ll want to back up essential files and replace your SSD.
  - File System Repair: Could indicate an issue with the connector port
    - Before action, backup integral files and then repair system
  - Crashing: Computer crashes while booting up but seems to work normally after several reboots
    - Run software to assess performance and health
    - Reinstall OS after partition set is cleared of data
  - Read-Only Mode: will not operate except to perform read-only functions
    - Save important data by backing up before seeking a solution

#### How do you fix a failed SSD?

- Formatting the Drive and Re-downloading the OS
- Power Cycling the SSD:
  - Unplug the SATA data cable (leave the power plugged in)
  - Leave the power on for 30 mins
  - Turn off power for 30 secs
  - Turn it back on and reconnect data cable
- Idling in the boot menu
  - Smilar to power cycling, but while the power is on during the 30 mins, the PC should be left to idle in boot menu
- Updating the SSD Firmware
  - Run a firmware update too to check for latest version
  - Install latest version, and wait for data access restoration
- Updating the drivers
  - In Windows, check Device Manager > Disk-Drives by right-clikcing the SSD to update and reboot

#### Is is possible to recover data from a failed SSD?

- TRIM (an advanced ATA command) helps an OS know which data blocks it can clear. THi sincreased both the performance and service life of an SSD by expediting data writing, but complicateds data recovery in the event of SSD corruption. TRIM erases data completely upon deletion
- This aside, there are tools that can make SSD storage achievable

#### SSD protection best practices

- Download a program from a selection of exiting software options designed to monitor SSD health by tracking operating temps and performance metrics
- When investing in a new SSD, ensure they come with SMART (Self-Monitoring, Analysis, and Reporting Technology)
- Have a backup strategy and always backup data regularly and routinely

### How to Erase a Hard Drive Using DBAN

- DBAN (Darik's Boot and Nuke):
  - Free Data Destruction Program to *completely* erase all files on a hard drive
  - Includes *everything*: application, personal files, and OS
  - Has to run while the OS is not in use
  - Has to be burnt to a disc/USB to run

#### Steps How to Erase a Hard Drive Using DBAN

1. Download [DBAN](https://sourceforge.net/projects/dban/)
2. Save the DBAN ISO file to PC
3. Burn DBAN to a [Disc](https://www.lifewire.com/how-to-burn-an-iso-image-file-to-a-dvd-2626156) or [USB](https://www.lifewire.com/how-to-burn-an-iso-file-to-a-usb-drive-2619270) *(cannot just copy and paste)*
4. Restart and boot into DBAN [Disc](https://www.lifewire.com/how-to-boot-from-a-cd-dvd-or-bd-disc-2626090) or [USB device](https://www.lifewire.com/how-to-boot-from-a-usb-device-2626091)
5. Choose an option from the DBAN main menu *(Designed to be used with keyboard only)*
6. Immediately start using DBAN with a Quick Command *(F3 in main menu)*
    - Commands used in DBAN:
        - dod
        - dodshort/autonuke
        - ops2
        - gutmann
        - prng
        - quick

7. Choose which hard drives to wipe with Interactive Mode
8. Wait for DBAN to erase the hard drive(s)
9. Verify DBAN has successfully erased the hard drive(s)
10. Remove the disc/USB, Shut Down, and Restart PC

## Things I want to know more about

- Which Bootable Discs/USBs are recommended for an IT/Cyber professional to have on hand
