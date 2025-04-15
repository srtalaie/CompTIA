## Honeypot
- Attract the bad guys
	- And trap them
- The "attackers" is probably a machine
	- Makes for interesting recon
- Honeypots
	- create a virtual world to explore
- Many different options
	- Most are open source and available to download
- Constant battle to discern the real from the fake
## Honeynets
- A real network includes more than a single device
	- Servers, workstations, routers, switches, firewalls
- Honeynets
	- Build a larger deception network with one or more honeypots
- More than one source of information
	- Stop spammers - https://projecthoneypot.org
## Honeyfiles
- Attract the attackers with more honey
	- Create files with fake information
	- Something bright and shiny
- Honeyfiles
	- Bait for the honeynet (ex/ passwords.txt)
	- Add many honeyfiles to file shares
- An alert is sent if the file is accessed
	- A virtual bear trap
## Honeytokens
- Track the malicious actors
	- Add some traceable data to the honeynet
	- If the data is stolen, you'll know where it came from
- ex/ API Credentials on public cloudshare
	- Does not actually provide access
	- Notifications are sent when used
- ex/ Fake email addresses
	- Add it to a contact list
	- Monitor the internet to see who posts it
- Many other honeytoken examples
	- Database records, browser cookies, web page pixels