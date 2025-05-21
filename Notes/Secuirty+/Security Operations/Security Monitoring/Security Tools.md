## Security Content Automation Protocol (SCAP)
- Many different security tools on the market
	- NGFWs, IPS, vulnerability scanners, etc.
	- They all have their own way of evaluating a threat
- Managed by National Institute of Standards and Technology (NIST)
	- [SCAP](http://scap.nist.gov)
- Allows tools to identify and act on the same criteria
	- Validate the security configuration
	- Confirm patch installs
	- Scan for a security breach
## Using SCAP
- SCAP content can be shared between tools
	- Focused on configuration compliance
	- Easily detect applications with known vulnerabilities
- Especially useful in large environments
	- Many different operating systems and applications
- This specification standard enables automation
	- Even between different tools
- Automation types
	- Ongoing maintenance
	- Notification and alerting
	- Remediation of noncompliant systems
## Benchmarks
- Apply security best-practices to everything
	- Operating systems, cloud providers, mobile devices, etc.
	- The bare minimum for security settings
- Example: Mobile device
	- Disable screenshots, disable screen recordings, prevent voice calls when locked, force encryption backups, disable additional VPN profiles, configure a "lost phone" message, etc.
- [Popular benchmarks - Center for Internet Security (CIS)](https://www.cisecurity.org/cis-benchmarks/)
## Agents/Agentless
- Check to see if the device is in compliance
	- Install a software agent onto the device
	- Run an on-demand agentless check
- Agents can usually provide more detail
	- Always monitoring for real-time notifications
	- Must be maintained and updated
- Agentless runs without a formal install
	- Performs the check, then disappears
	- Does not require ongoing updates to an agent
	- Will not inform or alert if not running
## SIEM
- Security Information and Event Manager
	- Logging of security events and information
- Log collection of security alerts
	- Real-time information
- Log aggregation and long-term storage
	- Usually includes advanced reporting features
- Data correlation
	- Link diverse data types
- Forensic analysis
	- Gather details after an event
## Anti-virus and anti-malware
- Anti-virus is the popular term
	- Refers specifically to a type of malware
	- Trojans, worms, macro viruses
- Malware refers to the broad malicious software category
	- Anti-malware stops spyware, ransomware, fileless malware
- The terms are effectively the same these days
	- The names are more of a marketing tool
	- Anti-virus software is also anti-malware software now
	- Make sure your system is using a comprehensive solution
## Data Loss Prevention (DLP)
- Where's your data?
	- Social security numbers, credit card numbers, medical records
- Stop the data before the attacker gets it
	- Data "leakage"
- So many sources, so many destinations
	- Often requires multiple solutions
	- Endpoint clients
	- Cloud based systems
		- Email, cloud storage collaboration tools
## SNMP
- Simple Network Management Protocol
	- A database of data (MIB) - Management Information Base
	- The database contains OIDs - Object Identifiers
	- Poll devices over udp/161
- Request statistics from a device
	- Server, firewall, workstation, switch, router, etc.
- Poll device at fixed intervals
	- Create historical performance graphs
## SNMP traos
- Most SNMP operations expect a poll
	- Devices then respond to the SNMP request
	- This requires constant polling
- SNMP traps can be configured on the monitored device
	- Communicates over udp/162
- Set a threshold for alerts
	- If the number of CRC errors increases by 5, send a trap
	- Monitoring station can react immediately
## NetFlow
- Gather traffic statistics from all traffic flows
	- Shared communication between devices
- NetFlow
	- Standard collection method
	- Many products and options
- Probe and collector
	- Probe watches network communication
	- Summary records are sent to the collector
## Vulnerability scanners
- Usually minimally invasive
	- Unlike a pentest
- Port scan
	- Poke around and see what's open
- Identify systems
	- And security devices
- Test from the outside and inside
	- Don't dismiss insider threats
- Gather as much information as possible
	- Not always accurate, requires going in afterwards and sorting out the details