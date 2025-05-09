## Zero Trust
- You have to authenticate or prove yourself anytime you want to gain to a resource
- Many networks are relatively open on the inside
	- Once you're through the firewall, there are few security controls
- Zero trust is a holistic approach to network security
	- Covers every device, every process, every person
- Everything must be verified
	- Nothing is inherently trusted
	- Multi factor authentication, encryption, system permissions, additional firewalls, monitoring and analytics, etc.
## Planes of operation
- Split the network into functional planes
	- Applies to physical, virtual, and cloud components
- Data plane
	- Part of device that is performing the actual security process
	- Process the frames, packets, and network data
	- Processing, forwarding, trunking, encrypting, NAT
- Control plane
	- Manages the actions of the data plane
	- Define policies and rules
	- ex/ Determines how packets should be forwarded
	- ex/ Routing tables (firewall rules), session tables, NAT tables
## Extend the physical architecture
- Separate into functional tasks
	- Incorporate into hardware or software
## Controlling trust
- Adaptive identity
	- Consider the source and the requested resources
	- Multiple risk indicators - relationship to the organization, physical location, type of connection, IP address, etc.
	- Make the authentication stronger, if needed
- Threat scope reduction
	- Decrease the number of possible entry points
- Policy-driven access control
	- Combine the adaptive identity with a predefined set of rules
## Security zones
- Security is more than a one-to-one relationship
	- Broad categorizations provide a security-related foundation
- Where are you coming from and where are you going
	- Trusted, untrusted
	- Internal network, external network
	- VPN 1, VPN 5, VPN 11
	- Marketing, IT, Accounting, Human Resources
- Using the zones may be enough by itself to deny access
	- ex/ Untrusted to Trusted zone traffic
- Some zones are implicitly trusted
	- ex/ Trusted to Internal zone traffic
## Policy enforcement point
- Subjects and systems
	- End users, applications, non-human entities
- Policy Enforcement Point (PEP)
	- The gatekeeper, all traffic must pass through this point
- Allow, monitor, and terminate connections
	- Can consist of multiple components working together
## Applying trust in the planes
- Policy Decision Point (PDP)
	- Examines the authenticate and decides whether it should be allowed on the network
	- There's a process for making an authentication decision
- Policy Engine
	- Evaluates each access decision based on policy and other information sources
	- Grant, deny, or revoke
- Policy Administrator
	- Communicates with the Policy Enforcement Point
	- Generates access tokens or credentials
	- Tells the PEP to allow or disallow access