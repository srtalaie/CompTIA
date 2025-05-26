## FIM (File Integrity Monitoring)
- Some files change all the time, some don't ever change
- Monitor important operating system and application files
	- Identify when changes occur
- Windows - SFC (System File Checker)
- Linux - Tripwire
- Many host-based IPS options
## Data Loss Prevention (DLP)
- Where's your data?
	- Social security numbers, credit card numbers, medical records
- Stop the data before the attackers get it
	- Data "leakage"
- So many sources, so many destinations
	- Often requires multiple solutions in different places
## Data Loss Prevention (DLP) systems
- On your computer
	- Data in use
	- Endpoint DLP
- On your network
	- Data in motion
- On your server
	- Data at rest
## USB blocking
- DLP on a workstation
	- Allow or deny certain tasks
- November 2008 -  U.S. Department of Defense
	- Worm virus "agent.biz" replicates using USB storage
	- Bans removable flash media and storage device
- All devices had to be updated
	- Local DLP agent handled USB blocking
- Ban was lifted in February 2010
	- Replaced with strict guidelines
## Cloud-based DLP
- Located between users and the internet
	- Watch every byte of network traffic
	- No hardware, no software
- Block custom defined data strings
	- Unique data for your organization
- Manage access to URLs
	- Prevent file transfers to cloud storage
- Block viruses and malware
	- Anything traversing the network
## DLP and email
- Email continues to be the most critical risk vector
	- Inbound threats, outbound data loss
- Check every email inbound and outbound
	- Internal systems or cloud-based
- Inbound
	- Block keywords, identify impostors, quarantine email messages
- Outbound
	- Fake wire transfers, W-2 transmissions, employee information
## Email a spreadsheet template
- November 2016
- Boeing employee emails spouse a spreadsheet to use as a template
- Contained the personal information of 36,000 Boeing employees
	- IN hidden columns
	- Social security numbers, date of birth, etc.
- Boeing sells its own DLP software
	- But only uses it for classified work