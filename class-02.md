# Class 02 Reading Notes

## Dev Tools

### Resources

- [GitHub](https://docs.github.com/en/get-started/quickstart/hello-world)
- [VS Code](https://code.visualstudio.com/docs)
- [Origins of Bash/Story of Shellshock](https://www.wired.com/2014/09/shellshocked-bash/)
- [Tutorialspoint - What is Shell?](https://www.tutorialspoint.com/unix/unix-what-is-shell.htm)

#### Github Introduction

- Code hosting platform for version control and collaboration.
- Allows everyone to work together on projects from anywhere.
- Github essentials: Repositories, Branches, Commits, and Pull Requests.
- GitHub Glossary: <https://docs.github.com/en/get-started/quickstart/github-glossary>

#### VS Code Introduction

- Lightweight, powerful, and free source code editor which runs on Desktops and is available for Windows, macOS, and Linux.
- Comes with built-in support for JavaScript, TypeScript, and Node.js and extensions of others (C++, C#, Java, Python, PHP, Go, .NET).
- It is managed by Microsoft..

#### Shellshock

- Shellshock: One of the oldest known and unpatched bugs in history.
- Shellshock: Continues to plague the internet and open source software.
- 1987: Built Bash for the UNIX OS during Free Software Movement by Fox and Stallman.
- late 1980s: Ramey took over from Fox as lead developer of Bash.
- September 12 (1980s): Ramey was updated with identified Shellshock bug.
- Ramey thinks he wrote the buggy code himself around in the early 90s.
- 1992: Engineer typed Shellshock into the bash code.
- Heartbleed is another bug in the open-source world.
- Bash has never had a full-blown security audit and is developed by a skeleton crew with virtually no fiancial support.
- This is due to something called Linus's Law that states: "If many eyes had been looking at bash over the past 25 years, these bugs would've been found a long time ago". This law was named after the guy that created the Linux OS
- Microsoft: After the Blaster worm in their OS in 2003, the company made security audits a priority.
- White-hat hackers/Pen Testers are keep contributors to that.

#### Shell

- Provides an interface to the Unix system.
- Original Unix shell was written in mid-1970s by Stephen R. Bourne while at AT&T Bells Labs in New Jersey.
- Gathers input from user and executes programs based on input.
- Environment to run commands, programs, and shell scripts.
- .sh = Script
- $ = Shell/Command Prompt
- shebang = #!/bin/sh (Alerts system that shell script is being started)
- A good shell script will have a # preceding comments
- Bourne shell was the first shell on Unix system, so it is known as *"the shell"*
- Bourne shell is usually installed as /bin/sh on most versions of Unix
- Two major Shell types in Unix are:
    1. Borne Shell ($ Default Prompt)
        - Subcategories:
            - Bourne Shell (sh)
            - Korn Shell (ksh)
            - Bourne Again Shell (bash)
            - POSIX Shell (sh)
    2. C Shell (% Default Prompt)
      - Subcategories:
            - C Shell (csh)
            - TENEX/TOPS C Shell (tcsh)

## Things I want to know more about

    - Debugging
    - Loops
    - Conditional Tests/Statements
