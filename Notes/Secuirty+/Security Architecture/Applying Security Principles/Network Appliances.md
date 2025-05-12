## Jump server
- Access secure network zones
	- Provides an access mechanism to a protected network
- Highly-secured device
	- Hardened and monitored
- SSH/Tunnel/VPN to the jump server
	- RDP, SSH, or jump from there
- A significant security concern
	- Compromise of the jump server is a significant breach
## Proxies
- Sits between the users and the external network
- Receives the user requests and sends the request on their behalf (the proxy)
- Useful for caching information, access control, URL filtering, content scanning
- Applications may need to know how to use the proxy (explicit)
- Some proxies are invisible (transparent)
## Application proxies
- One of the simplest "proxies" is a Network Address Translation (NAT), which will convert between internal or external IP addresses on internet facing routers
	- A network-level proxy
- Most proxies in use are application proxies
	- The proxy understands the way the application works
- A proxy may only know one application
	- HTTP
- Many proxies are multi-purpose proxies
	- HTTP, HTTPS, FTP, etc.
## Forward proxy
- An "internal proxy"
	- Commonly used to protect and control user access to the outside internet from the internal network
## Reverse proxy
- Inbound traffic from the internet  goes to the proxy server to your internal service
- Provides additional security in front of your web server, can also act as a caching server
## Open proxy
- A third-party, uncontrolled proxy
	- Can be a significant security concern
	- Often used to circumvent existing security controls
## Load balancer
- Distribute the load
	- Multiple servers4
	- Invisible to the end-user
- Large-scale implementations
	- Web server farms, database farms
- Fault tolerance
	- Server outages have no effect
	- Very fast convergence
## Active/active load balancing
All servers connected to the load balancer are active and being managed by the load balancer
- Configurable load
	- Manage across servers
- TCP offload, which means it doesn't have to set up an individual TCP sessions for each server
	- Protocol overhead
- SSL offload, instead of having servers manage encryption individually the load balancer handles the encryption of outbound data and decryption of inbound data to the servers
	- Encryption/Decryption
- Caching
	- Fast response
- Prioritization
	- QoS
	- Certain applications or protocols can be set to have a higher priority
- Content switching
	- Application-centric balancing
	- Can send certain requests to specific web servers under the load balancer
## Active/passive load balancing
- Some servers are active
	- Others are on standby
- If an active server fails, the passive server takes its place
## Sensors and collectors
- Aggregate information from network devices
	- Built-in sensors, separate devices
	- Integrated into switches, routers, servers, firewalls, etc.
- Sensors
	- Intrusion prevention systems, firewall logs, authentication logs, web server logs, database transaction logs, email logs
- Collectors
	- Proprietary consoles (IPS, firewall), SIEM (Security Information and Event Manager) consoles, syslog servers
	- Many SIEMs include a correlation engine to compare diverse sensor data
