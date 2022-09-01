# Class 08 Reading Notes

## Windows Registry Demystified

### Resources

- [Windows Registry Demystified](https://www.howtogeek.com/370022/windows-registry-demystified-what-you-can-do-with-it/)
- [How to use Windows Event Viewer](https://www.faqforge.com/windows/windows-10/what-is-event-viewer-and-how-to-use-it-in-windows-10/)
- [Edit the Windows Registry from the Command Prompt](https://www.howtogeek.com/677453/how-to-edit-the-windows-registry-from-the-command-prompt/)

## What You Can Do With It

The Windows Registry is a database where Windows and many programs store their configuration setting
    - Registry Hacks: Edit the registry to enable hidden features and tweak specific options

### What is the Windows Registry, and How Does It Work?

- It is a collection of several databases
- System-wide registry settings that apply to all users, and each user account has its own user-specific settings
- Registry contains folder-like "keys" and "values". Made up of multiple groups of keys and values called "hives" (one of the original developers of Windows NT hated bees)
- Keys can contain numbers, text, or other data
- Historically introduced back in Windows 3.1
  - Used only for certain types of software (apps frequently stored settings in .INI config files scattered across the OS)
- Some programs store all, some, or no settings in configuration files

- In Windows 10 and 7, you cannot edits these files directly:
  - Registry Path: C:\Windows\System32\Config\
  - User Account NTUSER.dat: C:\Windows\Users\Name
>
- You never need to touch registry file locations. When you:
  - Sign into Windows, loads the settings from files into memory
  - Launch a program, checks the registry stored in memory to find configuration settings
  - Change a program's settings, it changes the settings in the registry
  - Sign out of PC, it saves the state of the registry to the disk

### Why You Might Want to Edit the Registry

- Find Registry hacks online to help accomplish particular tasks

### Is It Safe?

- It is not dangerous if you know what you are doing
- Follow instructions and only change the settings you are instructed to change
- Pontentially can render Windows unbootable or applications broken
- Recommended to back up the registry (computer, too) before editing the registry

### How to Edit the Regitsry

- Open the Registry Editor application (by searching for it or by running the regedit.exe command in the search bar/run command)
- Agree to User Account Control prompt
- Navigate to whatever key you need to modify (can copy and paste an address into the address bar)
- To change value, double-click it and enter new value
- To create a new value, right-click in right pan, select the type of value, and enter appropriate name for it
- Select OK to save changes
- Close Registry Editor
- Sometimes a reboot/sign out is required for changes to take effect
- Can also edit it by downloading and running .reg files: text files that can open in Notepad and can be executed (only download them from sources you trust)
- You can make your own .reg file that automatically applies all your favorite registry hacks and configuration tweaks to a Windows PC when you run it

### Cool Registry Hacks For You To Try

- Display a Message at Sign In: You can make Windows always show a message whenever someone signs into your PC.
- Enable Windows Defender’s Secret Crapware Blocker: On Windows 10, Windows Defender automatically scans for malware in the background. It can protect you from “potentially unwanted programs” (PUPs) too if you change a registry setting.
- Clean Up Your Messy Context Menu: You can manually remove entries from the cluttered context menu on your desktop or in the file manager via the registry.
- Add Any Application to Your Desktop’s Context Menu: You can add any application to your desktop’s context menu. Right-click your desktop and select the entry to launch it quickly.
- Add “Open With Notepad” to the Context Menu for All Files: If you regularly find yourself looking at various types of text files in Notepad, add an “Open With Notepad” option to every file to make this faster.
- Stop Other User Accounts From Shutting Down Your PC: You can prevent specific user accounts on your PC from shutting it down by applying this registry hack.
- Block User Accounts From Running Specific Apps: Using the registry, you can prevent other Windows user accounts from running specific applications on your system.
- Make Your Taskbar Buttons Always Switch to the Last Active Window: This is my personal favorite. On Windows 7 and Windows 10, clicking your taskbar buttons normally shows you a thumbnail list of all your open windows for that application, if it has multiple windows open. The LastActiveClick hack makes a single click open your last active window for that application, saving you a click when switching windows. You can still hover over a taskbar icon to see previews of its open windows.
- Disable Windows 10’s Lock Screen: If you don’t like swiping away the tablet-style lock screen and want to see a traditional sign-in screen every time you boot, sign out of, or lock your PC, this registry hack is for you. It was created for Windows 8 but still works on the latest versions of Windows 10.
- Add “Take Ownership” to the Context Menu: On Windows, files are “owned” by users. If you’re an advanced user who changes file ownership frequently, you can add a “Take Ownership” command to the context menu to speed this up.
- Disable Aero Shake Minimizing of Windows: You can stop Windows 7 or Windows 10 from minimizing all your open windows whenever you shake a window’s title bar with this setting.
- Get the Old Volume Control Back on Windows 10: If you miss the Windows 7-style volume control, this registry hack will bring it back on Windows 10.
- Change the Manufacturer Name of Your PC: You can put your own name in the manufacturer field—which is especially cool if you built your own PC. You can even add your own logo.
- Remove the “3D Objects” Folder from This PC on Windows 10: Don’t like seeing the new “3D Objects” folder under This PC? This registry hack will remove it.
- Remove Folders From This PC on Windows 10: You can also hide the Desktop, Documents, Downloads, Music, Pictures, and Videos folders from the This PC view if you like.
- Remove OneDrive From File Explorer on Windows 10: If you don’t want to use OneDrive on Windows 10, this registry hack will remove its folder from File Explorer.
- Disable the “Low Disk Space” Check: Sick of Windows bugging you about low disk space on your PC? You can disable the check via the registry. This is particularly useful if Windows messes up and keeps warning you about a normally hidden recovery partition, for example.
- Stop Windows from Adding “- Shortcut” to New Shortcuts: Want to get rid of “- Shortcut” in the names of new shortcuts? Here you go.
- Disable SMBv1 on Windows 7 for Security: For security reasons, the old SMBv1 file sharing protocol is now disabled by default on Windows 8 and Windows 10. It’s still enabled by default on Windows 7 for compatibility reasons on business networks, but you can disable it for improved security.
  
## Things I want to know more about
