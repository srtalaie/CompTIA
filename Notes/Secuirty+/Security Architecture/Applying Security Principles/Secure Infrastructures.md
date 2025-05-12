## Device placement
- Every network is different
	- There are often similarities
- Firewalls
	- Separate trusted from untrusted
	- Provide additional security checks
- Other services may require their own security technologies
	- Honeypots, jump server,
	- load balancers, sensors
## Security zones
- Zone-based security technologies
	- More flexible (and secure) than IP address ranges
- Each area of the network is associated with a zone
	- Trusted, untrusted
	- Internal, external
	- Inside, Internet, Servers, Databases, Screened
- This simplifies security policies
	- Allowed to send data from Trusted to Untrusted
	- Allowed to send data from Untrusted to Screened
	- Allowed to send data from Untrusted to Trusted in certain circumstances
## Attack surface
- How many ways into your network
- Everything can be a vulnerability
	- Application code
	- Open ports
	- Authentication process
	- Human error
- Minimize the surface
	- Audit the code
	- Block ports on the firewall
	- Monitor network traffic in real-time
## Connectivity
- Everything contributes to security
	- Including the network connection
- Secure network cabling
	- Protect the physical drops
- Application-level encryption
- Network-level encryption
	- IPsec tunnels, VPN connections
