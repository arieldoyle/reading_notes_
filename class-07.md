# Class 07 Reading Notes

## OS Upgrade and Remote Access

### Resources

[Should You Learn Powershell?](https://techthoughts.info/ps1-should-you-learn-powershell/)

[Who needs malware?](https://www.theregister.com/2019/02/26/malware_ibm_powershell/)

[What is a Powershell attack?](https://www.youtube.com/watch?v=fe5Mbszdu9M)

[Microsoft Documentation: What is Powershell?](https://docs.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7)

[Microsoft Documentation: Getting Started with Powersehll](https://docs.microsoft.com/en-us/powershell/scripting/learn/ps101/01-getting-started?view=powershell-7)

[Quick Reference - Powershell Variables and Operators](https://ss64.com/ps/syntax-variables.html)

## Should You Learn Powershell?

### Introduction

- PowerShell:
  - Command-line shell interface made by Microsoft that enables system administrators and power users to manage computers from the command line
  - Scripting language, built on .NET (used for automating administrative tasks and configuration management)
  - Tasks are generally performed using cmdlet (command-let) can perform a wide variety of actions

### Other Languages Defined

- JavaScript
  - Client-side scripting language used to add interactive behavior to web pages. Typically paired with Javascript frameworks to build web and mobile apps
  >
- Java
  - A programming language used to create applicatio (android, server, web) as well as various software tools.
  >
- Python
  - A general purpose programming language that can create desktop GUI Applications, websites, web applications, as well as carry out a wide array of automation tasks.
  >
- C#
  - A general purpose language designed for developing applications. Often used for Windows desktop applications and games. Also used for web applications as well as mobile development.
  >
- Ruby
  - A general purpose language typically combined with Rails (a development tool with a focus of RESTful application design). Rails is one of the most popular web development frameworks today. Ruby by itself is a very flexible language used to rapidly build applications.
  >
- PowerShell vs Other Languages
  - Commonality between the other languages is that they *create* something:
    - Desktop / Web Application / Website / Game / Mobile App
  - PowerShell is the language for *doing* things in context to managing a technology environment

### Who Uses PowerShell?

- Developers / Administrators / Engineers / Architects

### What's in a Shell?

- Linux > Bash > Python
- Windows > PowerShell > C#

### PowerShell vs Bash

Both rely on concept of pipeline, except:

- Bash pushes around globs of text
- PowerShell passes around the output of one cmdlet as the input for another one
>
- PowerShell:
  - Microsoft command-line shell and associated scripting language used for task automation and configuration management
  - Works with Objects
  - PowerShell is not just a shell; it is a complete scripting environment.
  - PowerShell scripts share complex data, passing entire data objects structures between commands
  >
- Bash:
  - Shell primary used in Linux
  - Combines scripting language, as well as a host of native Linux tools to automate/manage Linux devices
  - Unix shell and command language used for task automation and management
  - Works with strings
  - Bash, the "veteran IT soldier" passes output and input as plain text (Makes it easy to move move information to the next program)

### Strings vs Objects

- Bash requires lots of string manipulation and parsing to get info you want
- PowerShell very easily pass objects between cmdlets, allowing you to move complex data with very little effort

### Where can you use PowerShell?

- Windows
- Linux
- Hyper-V
- VMWare
- AWS
- Azure
- Oracle

### Why you should learn PowerShell

- PowerShell Advantages:
  - Automation: faster
  - Accuracy: reduce mistakes
  - Versatility: learning once enhances you everywhere
  - Community: connected tech community
  - Relevant: Continues to grow and be adopted

### Beginning your path to learn PowerShell

- [YouTube Channel](https://www.youtube.com/channel/UC2iX3Hd2za22bOozudNZEuA)
- Can spin up VMs in Azure, upload objects to AWS S3, or manage Windows environment efficiently

## Who needs malware? IBM says most hackers just PowerShell through boxes now, leaving little in the way of footprints

## Things I want to know more about

- 2018: IBM's X-Force found 43% of attacks it analyzed utilized any sort of locally installed files. Rather, hackers utilized PowerShell scripts to execute their dirty deeds in memory without significantly touching file systems
- Reminder that admins can no longer solely rely on detecting malicious executiables and similar data on hard drives and other storage, to identify cyber-intrusions

- Languages in general
  - Java
  - Python
  - JavaScript
  - PowerShell
