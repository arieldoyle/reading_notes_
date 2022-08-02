# Class 06 Reading Notes

## Windows Security Center

### Resources

[Windows Defender Security Center](https://www.thewindowsclub.com/windows-defender-security-center)

[Article - How to use Windows Event Viewer](https://www.faqforge.com/windows/windows-10/what-is-event-viewer-and-how-to-use-it-in-windows-10/?WPACFallback=1&WPACRandom=1659388000913)

## Windows Defender Security Center in Windows 10

- In windows 10v1703 and later: White Shield Icon in notification area on Taskbar
- To Open: Right-click icon and select Open the Windows Defender Security Center
- Dashboard: Tool for all security features to give a cleaner view of any risks your PC may face to help simplify and unify all security settings of Windows into the same place (even third-party security)
- If an issue that requires your attention is found, you will see a yellow exclamation mark icon overlay on the shield icon (click on View Health Report Button)
- Click Open Troubleshooter to help fix issues
  - Virus & threat protection
    - Launches third-party AV Protection app directly
    - Displays scan results and threat history
    - Can control and use the Controlled Folder Access to protect data against ransomware attacks
    >
  - Device performance & health
    - Monitors battery life and storage capacity
    - Complete view of latest Windows updates, and drivers
    - Option to restore or refresh Windows
    >
  - Firewall & network protection
    - Manages Windows Firewall settings
    - Manages links to network troubleshooting info
    - Provides information on local networks in the Network and sharing center control panel option
    >
  - App & browser control
    - Enables adjustments in settings of SmartScreen for apps and browsers for online warnings
    >
  - Family Options
    - View health and safety of family devices
    - Configure options for parental controls and options for:
      - Habits
      - Activity of your kids' online activity
      - Manage controls for limiting access to purchasing games and apps online
    >
  - Settings
    - Toggles the Windows Defender and Windows Firewall notifications
    - Virus & threat protection settings (to configure Windows Defender)
    - Disable Windows Defender Security Center taskbar icon
    - Increases support for Windows Hello  

## What is Event Viewer and How to Use it in Windows 10

- Introduction - What is the Event Viewer?
  - Views the details log of all our applications by giving us:
    - Detailed analysis of the working of all the applications in Windows 10
    - List of all the error events that occurred while running any application
    - Helps us to determine the root cause of all the problems
    - Facilitates us in tracing applications that cause problems while running
    - Increases efficiency of your computer system
    - Saves you in the future from some of the most commonly occurring issues
>
- Using Even Viewer:
  - Type Event Viewer in Search of taskbar
  - Click Event Viewer to launch
  - Application Log: Records those events that are related to the interface and other important components that are necessary for an application to run
    - Three levels:
      - Information: Inform about the normal activity of an application
      - Error: Inform about the occurrence of an error while running an application
      - Warning: Tells about any possible issues that may occur while running the application
      >
  - Security log: Concerned with the evens related to login attempts and other security features of Windows 10
      -Two levels:
        - Audit Success: ID the successful login attempts
        - Audit Failure: ID the failed login attempts
        >
  - System Log: Tracks those events that are related to the pre-installed programs of Windows 10
    - Three levels:
      - Information: same as above
      - Error: same as above
      - Warning: same as above
  >
  - Windows Log: View the number of events of each type and the size occupied by those events under the Windows Logs
  >
- Conclusion:
  - Use Event Viewer to analyze the Event Log in order to know all about the even that occur on your PC using Windows 10

## Things I want to know more about
