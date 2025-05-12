## Intrusion Prevention System (IPS)
- Intrusion Prevention System
	- Watch network traffic
- Intrusions 
	- Exploits against operating systems, applications, etc. 
	- Buffer overflows, cross-site scripting, other vulnerabilities
- Detection vs. Prevention
	- Intrusion Detection System (IDS) - Alarm or alert
	- Prevention - Stop it before it gets into the network
## Failure modes
- We hope for 100% uptime
	- This is not realistic
	- Eventually something will break
- Fail-open
	- When a system fails, data continues to flow
- Fail-closed
	- When a system fails, data does not flow
## Device connections
- Active monitoring
	- System is connected inline
	- Data can be blocked in real-time as it passes by
	- Intrusion prevention is commonly active
		- IPS sits between the fire-wall and the end device
			- After data passes from the internet through the firewall the IPS makes the decision of whether to let it pass through or stop it
			- IPS constantly monitoring the traffic
	- Some concerns of having it always on:
		- An outage may cause downtime for the rest of the network
		- IPS might be too aggressive with blocking traffic and may be blocking legitimate traffic instead of malicious traffic
- Passive monitoring
	- A copy of the network traffic is examined using a tap or port monitor
	- Data cannot be blocked in real-time
	- Intrusion detection is commonly passive
	- Has limited capabilities in terms of blocking traffic
## Active monitoring
- IDS/IPS sits physically inline
	- All traffic passes through the IDS/IPS
- IPS is where it will be evaluated
- The IPS can identify potential attacks and block them immediately
## Passive monitoring
- Requires you have something that is able to create and send a copy of the network traffic
	- Port mirror (SPAN), network tap
- No way to block (prevent) traffic
	- Common with IDSs
- Passive monitoring uses a combination of an IDS and IPS
	- When traffic reaches the IDS it creates a copy of the data and sends one copy down the line and another to the IPS where it is analyzed for malicious activity