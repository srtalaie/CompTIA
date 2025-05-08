## Replay attack
- Useful information is transmitted over the network
	- A crafty hacker will take advantage of this
- Need access to the raw network data
	- Network tap, ARP poisoning, Malware on victim's computer
- The gathered information may help the attacker
	- Replay the data to appear as someone else
- This is not an on-path attack
	- The actual replay doesn't require the original workstation
## Pass the hash
- The hash here being the password hash used during the authentication process
- How it works
	- The client/victim sends a normal auth request to the server
	- During that process the attacker has placed a way to redirect or get a copy of that traffic. Here being a username and hashed password
	- Now the hacker can replay the username and hashed password to the server posing as the original client
	- The server receives the correct username and hashed password matching a valid account so it gives the attacker access
- Avoid this type of replay attack with a salt or encryption
- Use a session ID with the password hash to create a unique authentication hash each time
## Browser cookies and session IDs
- Cookies
	- Information stored on your computer by the browser
- Used for tracking, personalization, session management
	- Not executable, not generally a security risk
		- Unless someone gets access to them
- Could be considered a privacy risk
	- Lots of personal data in there
- Session IDs are often stored in the cookie
	- Maintains sessions across multiple browser sessions
## Session hijacking (Sidejacking)
- A victim initially authenticates with a web server providing a username and password. In return the server provides the user with a session ID
- If the attacker gains access to the session ID they can then return that same ID to the web server giving the access to everything the victim has on that web server
## Header manipulation
- Information gathering
	- Wireshark, Kismet
- Exploits
	- Cross-site scripting
- Modify headers
	- Tamper, Firesheep, Scapy
- Modify cookies
	- Cookies Manager+ (Firefox add-on)
## Prevent session hijacking
- Encrypt end-to-end
	- They can't capture your session ID if they can't see it
	- Additional load on the web server (HTTPS)
	- Firefox extension: HTTPS Everywhere, Force-TLS
	- Many sites are now HTTPS-only
- Encrypt end-to-somewhere
	- At least avoid capture over local wireless network
	- Still in-the-clear for part of the journey
	- Personal VPN