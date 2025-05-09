## Technical change management
- Put the change management process into action
	- Execute the plan
- There's no such thing as a simple upgrade
	- Can have many moving parts
	- Separate events may be required
- Change management is often concerned with "what" needs to change
	- The technical team is concerned with "how" to change it
## Allow list/deny list
- Any application can be dangerous
	- Vulnerabilities, trojan horses, malware
- Security policy can control app execution
	- Allow list, deny/block list
- Allow list
	- Nothing runs unless it's approved
	- Very restrictive
- Deny list
	- Nothing on the "bad list" can be executed
	- Anti-virus, anti-malware
## Restricted activities
- The scope of a change is important
	- Defines exactly which components are covered
- A change approval isn't permission to make any change
	- The change control approval is very specific
- The scope may need to be expanded during the change window
	- It's impossible to prepare for all possible outcomes
- The change management process determines the next steps
	- There are processes in place to make the change successful
## Downtime
- Services will eventually be unavailable
	- The change process can be disruptive
	- Usually scheduled during non-production hours
- If possible, prevent any downtime
	- Switch to secondary system, upgrade the primary, then switch back
- Minimize any downtime events
	- The process should be as automated as possible
	- Switch back to secondary if issues appear
	- Should be part of the backout plan
- Send emails and calendar updates
## Restarts
- It's common to require a restart
	- Implement the new configuration
	- Reboot the OS, power cycle the switch, bounce the service
	- Helps you understand if the system can recover from a power outage?
- Services
	- Stop and restart the service or daemon
	- May take seconds or minutes
- Applications
	- Close the application completely
	- Launch a new application instance
## Legacy applications
- Some applications were here before you arrived
	- They'll be here when you leave
- Often no longer supported by the developer
	- You're now the support team
- Fear of the unknown
	- Face your fears and document the system
	- It may not be as bad as you think
- May be quirky
	- Create specific processes and procedures
- Become the expert
## Dependencies
- To complete A, you must complete B
	- A service will not start without other active services
	- An application requires a specific library version
- Modifying one component may require changing or restarting other components
	- This can be challenging to mange
- Dependencies may occur across systems
	- Upgrade the firewall code first
	- Then upgrade the firewall management software
## Documentation
- It can be challenging to keep up with changes
	- Documentation can become outdated very quickly
	- Require with the change management process
- Updating diagrams
	- Modifications to network configurations
	- Address updates
- Updating policies/procedures
	- Adding new systems may require new procedures
## Version control
- Track changes to a file or configuration data over time
	- Easily revert to a previous setting
- Many opportunities to manage versions
	- Router configurations
	- Windows OS patches
	- Application registry entries
- Not always straightforward
	- Some services and operating systems provide version control features
	- May require additional management software
