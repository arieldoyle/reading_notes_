# Class 05 Reading Notes

## Windows Command Line Tools

### Resources

[UpGuard: What is an SMB Port - Ports 445 and 139 Explained](https://www.upguard.com/blog/smb-port)

[A+ Certification Cheat Sheet](https://gcit.enschool.org/ourpages/auto/2017/8/2/56105037/220%20901%20Cheat%20Sheet%202017.pdf)

[Professor Messer: Microsoft Command Line Tools - CompTIA-220-1002 - 1.4](https://www.professormesser.com/free-a-plus-training/220-1002/microsoft-command-line-tools/)

## UpGuard: What is an SMB Port? A Detailed Description of Ports 445 + 139

### 1. How does the SMB Protocol Work?

- Server Message Block Protocol (SMB) is a client-server communication protocol used for sharing access to:
  - Files
  - Printers
  - Serial Ports
  - Data on a network
  - Transaction protocols for authenticated inter-process communication
>
- Enables users/applications to make requests for files on a remote server to:
  - Open  - Read - Move - Create - Update Files
>
- 1983: Originally designed by Barry Feigenbaum at IBM to run on top of NetBIOS over TCP/IP (NBT) using IP port 139 and UDP ports 137 and 138
  - Software application that run on NetBIOS sesssions locate and identify each other via their NetBIOS names over TCP port 139
>
- 1990: Microsoft merged SMB with LAN Manager product and continues to add features to the protcol in Windows for Workgroups
>
- 1996: Microsoft launched initiative to rename SMB to Common Internet File System (CIFS) and added more features to support:
  - Symbolic Links
  - Hard Links
  - Larger Files Sizes
  - Direct Connections over TCP port 445 without requiring NetBIOS as a transport
>
- 2000: Microsoft had changed SMB to operate over port 445 and it still uses it today
  - Problematic due to it taking 10% of network traffic (chatty protocol)
  - Explained that SMB 1.0 is block-level (rather than streaming) and for small LANs
  - SMB 2.0 improved the efficiency by reducing 100s of commands/subcommand down to 19
  - SMB 3.0 (introduced with Windows 8 and Windows Server 2012) added functionality mostly in the virtualized data centers and introduced end-to-end encryption and a new AES-based signing algorithm
  - Continues to invest in improving SMB performance and security today

### 2. What are the SMB Protocol Dialects?

- SMB 1.0 (1984):
  - Created by IBM for file sharing in DOS
  - Introduced locking as a client-side caching mechanism designed to reduce network traffic
>
- Samba (1992):
  - Open-source SMB and Microsoft Active Directory for Unix and Linux
  - Supports the below between Linux/Unix and Windows clients:
    - File Sharing
    - Print Services
    - Authentication
    - Authorization
    - Name Resolution
    - Service Announcements
>
- CIFS (1996):
  - Debuted in Windows 95
  - Added support for:
    - Larger File Sizes
    - Transport directly over TCP/IP
    - Symbolic Links
    - Hard Links
>
- NQ (1998):
  - Family of portable SMB
  - Developed by Visuality Systems
  - Portable to non-Windows platforms like Linux, iOS, and Android
  - Supports SMB 3.1.1 dialect
>
- Netsmb (2004):
  - Family of in-kernal SMB in BSD OS
>
- SMB 2.0 (2006):
  - Released with Windows Vista and Windows Server 2008
  - Reduced chattiness that:
    - Improved profermance
    - Enhanced Scalability and Resiliency
    - Supported WAN Acceleration
>
- Tuxera SMB (2009):
  - Proprietary SMB
  - Runs in Kernal or User-Space
>
- SMB 2.1 (2010):
  - Introduced with Windows Server 2008 R2 and Windows 7
  - Replaced the client Opportunistic Locking with Oplock Leasing Model that:
    - Enhanced caching
    - Improved performance
    - Introduced large Maximum Transmission Unit (MTU) support
    - Improved energy Efficiency
  - Overall enabling clients to open files from an SMB server to enter sleep mode
>
- SMB 3.0 (2012):
  - Introduced with Windows 8 and Windows Server 2012
  - Introduced several significant improvements to:
    - Availability
    - Performance
    - Backup
    - Security
    - Management
>
- MoSMB (2012):
  - Proprietary SMB for Linux and other Unix-like systems
  - Developed by Ryussi Technologies
  - Supports only SMB 2.x and SMB 3.x
>
- SMB 3.02 (2014):
  - Introduced with Windows 8.1 and Windows Server 2012 R2
  - Performance Updates
  - Ability to disable CIFS/SMB 1.0 support (removal of related binaries)
>
- SMB 3.1.1 (2015):
  - Introduced with Windows 10 and Windows Server 2016
  - Support for advanced encryption
  - Preauthentication integrity to prevent MitM attacks
  - Cluster dialect fencing

### 3. What are Ports 139 and 445?

- SMB requires an open port on a PC or server to communicate with other systems
- Generally over port 139 and 445
- Port 139:
  - Communicates over NetBIOS
  - Transport layer protocol used in Windows OS systems over a network
- Port 445:
  - Newer version of SMB (after Windows 2000) on top of a TCP stack
  - Allows SMB to communicate over the internet
  - Use IP addresses in order to use SMB like file sharing

### 4. Are Open Ports Dangerous?

- Ports 139 and 445 are not inherently dangerous, but they do have known issues
- Check if a port is open by using the netstat command
- Open ports are necessary to communicate accross the internet
- Open ports can become a security risk when the service listening to the port is:
  - Misconfigured
  - Unpatched
  - Vulnerable to exploits
  - Poor Network Security Ruled
- Most dangerous ports are wormable ports (open by default in some OS)
- SMB was exploited during the WannaCry ransomware attack through a zero-day exploit called EternalBlue
  - WannaCry exploited outdated versions of SMB
  - Network worm with a transport mech designed to auto spread itself
  - Transport code scans for systems vulnerable to EternalBlue Exploit and then installs DoublePulsar (backdoor tool), and executes a copy of itself
  - Infected CPs will:
    - Search for devices accepting traffic on TCP ports 135-139 or 445
    - Initiate an SMBv1 connections to the device
    - Use buffer overflow to take control of the system
    - Install randsomware component of attack
- Windows has since released a security update to prevent this exploit in:
  - Windows XP - Server 2003 - 8 - Vista - 7 - 8.1 - 10 - Server 2008 - Server 2008 R2 - Server 2012 - Server 2016
>
- How to keep Ports 139 and 445 Secure:
  - Avoid Exposing SMB Ports
  - Patch Everything
  - No Single Point of Failure
  - Use a Firewall or Endpoint Protection
  - Use a Virtual Private Network (VPN)
  - Implement Virtual Local Area Networks (VLANs)
  - Use MAC Address Filtering

## Windows Troubleshooting Utilities for the A+ Certification Exam

- chkdsk.exe = Check Disk: Check your hard drive for problems with the file
system and for bad sectors.
- regedit.exe = Registry Editor: Make changes to Registry values; can be used to
make selective backups. Prior to Windows XP, there were two editors: regedit.exe and regedt32.exe.
- defrag.exe = Disk Defragmenter: Used from the command line, or graphically through
the Microsoft Management Console (MMC) and dfrg.msc.
- sfc.exe = System File Checker: Verifies that system files have not been modified;
or, if they have, replaces them with the original. It works with the hidden
C:\windows\system32\dllcache directory and the original operating system CD.
- taskmgr.exe = Task Manager: See running programs and services, terminate
problems, and view rudimentary performance information about the system.
- perfmon.exe = Performance Console: View detailed performance information
- msconfig.exe = System Configuration Tool: Reconfigure the boot process for troubleshooting and diagnosing the boot process.
- msinfo32.exe = System Information: View hardware and configuration information for
your computer.
- tasklist.exe = Task List: Display a list of running applications or services on a
computer.
- taskkill.exe = Task Kill: Terminate a running application or service on a computer.
- gpupdate.exe = Group Policy Update: Re-process Active Directory (AD) Group Policy
Objects (GPO) on the computer.
- gpresult.exe = Group Policy Results: Evaluate the resultant policy results and list all GPOs which apply to the current computer or user.
- eventvwr.msc = Event Viewer: Logging component of the operating system; the
central location for all logging activity.
- ipconfig: Display basic TCP/IP configuration, such as IP address, subnet mask, and
default gateway.
- ipconfig /all: Display TCP/IP settings, including your Media Access Control (MAC)
address, domain name system (DNS) server, and lease information.
- ipconfig /release: Release your IP address.
- ipconfig /renew: Renew your IP address.
- ping IP address or ping host name: Send four test messages to the IP address or
host name you specify; verify whether the other system is up and running.
- netstat: Display TCP/IP protocol statistics and connection information. Can be used to
see who is connected to your system; what ports are open; and if you use an -o switch,
what the process ID is of the program that opened the port.
- nbtstat: Troubleshoot NetBIOS over TCP/IP. For example, you can view a remote
NetBIOS name table using nbtstat -a IP address.
- nslookup: Troubleshoot DNS problems. For example, you can get a listing of all the
records in DNS using nslookup.
- arp: Troubleshoot ARP. For example, you can use arp -a to view your Address Resolution
Protocol (ARP) cache.
- Tasklist: View a list of running processes.
- Taskkill /PID pid /F: Terminates a process when you supply the process id.

## Professor Messer: Microsoft Command Line Tools - CompTIA-220-1002 - 1.4

- Priviledges are important: user vs administrator
- Run Command Prompt as Admin to use it for elevated priviledges
- Use help or help copy (to get more information)
- [command] /? (to get more information on that command)
- cls (to clear the screen)
- dir (to see all directories in current directory)
- cd (change directory)
- .. (cd to the directory above where you are)
-shutdown
  - shutdown /s /t nn (to tell the PC to shutdown in certain amount of seconds)
  - shutdown /r /t nn (to tell the PC to restart in certain amount of seconds)
  - shutdown /a (cancel the shutdown command)
- dism (deployment image servicing and management tool) for editting WIM (window images)
  - dism /Get-WIMInfo /WinFile:d:\sources\boot.wim (tell what you want to do, what file to do it on, and where the file is located)
- sfc (system file check)
  - sfc /scannow (scans the OS files)
- chkdsk /f (fixes errors on disk)
- chkdsk /r (tries to recover bad sectors)
- diskpart (manage disk configs)
  - help = summary of options
  - create - format - list - list volume
- tasklist (list all operating tasks)
- taskkill /pid 3192 /t (with the pid)
- Group Policy (active directory) usually updated at login
  - gpupdate /target:"" /force
  - gpresult /r
  - gpresult user
- format (deletes everything on that specific disk/partition)
- copy (/v /y)
  - copy /v foldername and destination (verifies that all files were copied completely)
  - copy /y (overwrites an existing destination file)
  - copy /v /y (overrides the prompt for automation)
  - xcopy /s 'foldername and destination' (copies all the folders and subfolders)
  - robocopy (good for any copies that were interrupted)
    - robocopy /s 'foldername and destination'

## Things I want to know more about

- NetBIOS
- Oplock leasings vs Opportunistic locking
- Dialect Fencing (Cluster)
- netstat command
- WannaCry
- EternalBlue
- DoublePulsar
