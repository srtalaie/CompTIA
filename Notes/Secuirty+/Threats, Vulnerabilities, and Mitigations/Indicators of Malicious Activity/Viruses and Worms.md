## Virus
- Malware that can reproduce itself
	- It needs you to execute a program
- Reproduces through file systems or the network
	- Just running a program can spread a virus
- May or may not cause problems
	- Some viruses are invisible, some are annoying
- Anti-virus is very common
	- Thousands of new viruses each week
	- Is your signature file updated?
## Virus types
- Program viruses
	- It's part of the application
- Boot sector viruses
	- Trigger next time you boot up your computer
- Script viruses
	- Operating system and browser based
- Macro viruses
	- Common in Microsoft Office
## Fileless virus
- A stealth attack
	- Does a good job of avoiding anti-virus detection
- Operates in memory
	- But never installed in a file or application
- How it works
	- User clicks on malicious website link
	- Website exploits a Flash/Java/Windows vulnerability
	- Launches PowerShell and downloads payload in RAM
	- Runs PowerShell and executables in memory, exfiltrating data, damaging files
	- Adds an auto-start to Registry
## Worms
- Malware that self-replicates
	- Doesn't need you to do anything
	- Uses the network as a transmission medium
	- Self-propagates and spreads quickly
- Worms are pretty bad things
	- Can take over many systems very quickly at the speed of your network
- Firewalls and IDS/IPS can mitigate many worm infestations
	- Doesn't help much once the worm is inside