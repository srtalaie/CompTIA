## Segmenting the network
- Physical, logical or virtual segmentation
	- Devices, VLANs (network switches), virtual networks
- Performance
	- High-bandwidth applications
- Security
	- Users should not talk directly to database servers
	- The only applications in the core are SQL and SSH
- Compliance
	- Mandated segmentation (ex/ Payment Card Industry (PCI) compliance)
	- Makes change control much easier
## Access control lists (ACLs)
- Allow or disallow traffic
	- Groupings of categories
	- Source IP, Destination IP, port number, time of day, application, etc.
- Restrict access to network devices
	- Limit by IP address or other identifier
	- Prevent regular user/non-admin access
- Be careful when configuring these
	- You can accidentally lock yourself out
## Examples of ACLs
- List the permissions
	- Bob can read files
	- Fred can access the network
	- James can access network 192.168.1.0/24 using TCP ports 80, 443, and 8088
- Many operating systems use ACLs to provide access to files
	- A trustee and the access rights allowed
## Application allow list/deny list
- Any application can be dangerous
	- Vulnerabilities, trojan horses, malware
- Security policy can control app execution
	- Allow list, deny/block list
- Allow list
	- Nothing runs unless it's approved
	- Very restrictive
- Deny/Block list
	- Nothing on the "bad list" can be executed
	- ex/ Anti-virus, anti-malware
## Examples of allow/deny list
- Decisions are made in the operating system
	- Often built-in to the operating system management
- Application hash
	- Only allows applications with this unique identifier
- Certificate
	- Allow digitally signed apps from certain publishers
- Path
	- Only run applications in these folders
- Network zone
	- The apps can only run from this network zone

