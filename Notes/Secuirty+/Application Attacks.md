## Injection attacks
- Code injection
	- Adding your own information into a data stream
- Enabled because of bad programming
	- The application should properly handle input and output
- So many different injectable data types
	- HTML, SQL, XML, LDAP, etc.
## Buffer overflows
- Overwriting a buffer of memory
	- Spills over into other memory areas
- Developers need to preform bounds checking
	- The attacker spends a lot of time looking for openings
- Not a simple exploit
	- Takes time to avoid crashing things
	- Takes time to make it do what you want
- A really useful buffer overflow is repeatable
	- Which means that a system can be compromised
## Replay attack
- Useful information is transmitted over the network
	- A crafty hacker will take advantage of this
- Need access to the raw network data
	- Network tap, ARP poisoning, Malware on victim computer
- The gathered information may help the attacker
	- Replay the data to appear as someone else
- This is not an on-path attack
	- The actual replay doesn't require the original workstation
## Privilege escalation
- Gain higher-level access to a system
	- Exploit a vulnerability
	- Might be  bug or design flaw
- Higher-level access means more capabilities
	- This commonly is the highest-level access
	- This obviously is a concern
- These are high-priority vulnerability patches
	- You want to get these holes closed very quickly
	- Any user can be an administrator
- Horizontal privilege escalation
	- User A can access User B resources
## Mitigating privilege escalation
- Patch quickly
	- Fix the vulnerability
- Updated anti-virus/anti-malware software
	- Block known vulnerabilities
- Data Execution Prevention
	- Only data in executable areas can run
- Address space layout randomization
	- Prevent a buffer overrun at a known memory address
## Elevation of privilege vulnerability
- CVE-2023-29336
	- Win32k Elevation of Privilege Vulnerability
	- May 2023
	- Win32k Kernel driver
		- Server 2008, 2008 R2, 2012, 2012 R2, 2016
		- Windows 10
	- Attacker gain SYSTEM privileges
		- The highest level of access
## Cross-site requests
- Cross-site requests are common and legitimate
	- You visit professermesser.com
	- Your browser loads text from the professermesser.com server
	- Your browser loads a video from YouTube
	- Your browser loads pictures form Instagram
- HTML on professermesser.com directs requests from your browser
	- This is normal and expected
	- Most of these are unauthenticated requests
## The client and the server
- Website pages consist of client-side code and server-side code
- Client side
	- Renders the page on the screen
	- HTML, JavaScript
- Server side
	- Performs requests from the client
	- HTML, PHP
	- ex/ Transfer money from one account to another or Post a video on YouTube
## Cross-site request forgery
- One-click attack, session riding
	- XSRF, CSRF (sea surf)
- Takes advantage of the trust that a web application has for the user
	- The website trusts your browser
	- Requests are made without you consent or knowledge
	- ex/ Attacker posts a Facebook status on your account
- Significant web application development oversight
	- The application should have anti-forgery techniques added
	- Usually a cryptographic token to prevent forgery
- How it works:
	- You have an attacker, a bank site visitor, and a bank web server
	- Attacker creates a funds transfer request and send it to the visitor
	- The request is sent as a hyperlink to a user who may already be logged in to the bank web site
	- Visitor clicks the link and unknowingly sends the transfer request to the bank web site
	- Bank validates the transfer and sends the visitors' funds to the attacker
## Directory traversal
- Directory traversal/path traversal
	- Read files from a web server that are outside of the website's file directory
	- Users shouldn't be able to browse the Windows folder
- Web server software vulnerability
	- Won't stop users from browsing past the web server root
- Web application code vulnerability
	- Take advantage of badly written code