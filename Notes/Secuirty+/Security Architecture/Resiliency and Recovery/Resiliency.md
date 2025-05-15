## High availability
- Redundancy doesn't always mean always available
	- May need to be powered on manually
- HA (High Availability)
	- Always on, always available
- May include many different components working together
	- Active/Active can provide scalability advantages
- Higher availability almost always means higher costs
	- There's always another contingency you could add
	- Upgraded power high-quality server components, etc.
## Server clustering
- Combine two or more servers
	- Appears and operates as a single large server
	- Users only see one device
- Easily increase capacity and availability
	- Add more servers to the cluster
- Usually configured in the operating system
	- All devices in the cluster commonly use the same OS
## Load balancing
- Load is distributed across multiple server
	- The servers are often unaware of each other
- Distribute the load across multiple devices
	- Can be different operating systems
- The load balancer adds or removes devices
	- Add a server to increase capacity
	- Remove any servers not responding
## Site resiliency
- Recovery site is prepped
	- Data is synchronized
- A disaster is called
	- Business processes failover to the alternate processing site
- Problem is addressed
	- This can take hours, weeks, or longer
- Revert back to the primary location
	- The process must be documented for both actions
## Hot site
- An exact replica
	- Duplicates everything
- Stocked with hardware
	- Constantly updated
	- You buy two of everything
- Applications and software are constantly updated
	- Automated replication
- Flip a switch and everything moves
## Cold site
- No hardware
	- An empty building
- No data
	- Bring it with you
- No people
	- Bus in your team
## Warm site
- Somewhere between cold and hot
	- Just enough to get going
- Big room with rack space
	- You bring the hardware
## Geographic dispersion
- These sites should be physically different than the organization's primary location
	- Many disruptions can affect a large area
	- Hurricane, tornado, flood, etc.
- Can be a logistical challenge
	- Transporting equipment
	- Getting employee's on-site
	- Getting back to main office
## Platform diversity
- Every operating system contains potential security issues
	- You can't avoid them
- Many security vulnerabilities are specific to a single OS
	- Windows vulnerabilities don't commonly affect Linux or macOS
	- And vice versa
- Use many different platforms
	- Different applications, clients, and OSes
	- Spread the risk around
## Multi-cloud systems
- There are many cloud providers
	- Amazon Web Services, Microsoft Azure, Google Cloud, etc.
- Plan for cloud outages
	- Just because one provider is out does not mean the others are
- Data is both geographically dispersed and cloud service dispersed
	- A breach with one provider would not affect the others
	- Plan for every contingency
## Continuity of operations planning (COOP)
- Not everything goes according to plan
	- Disasters can cause disruption to the norm
- We rely on our computer systems
	- Technology is pervasive
- There needs to be an alternative
	- Manual transactions
	- Paper receipts
	- Phone calls for transaction approvals
- These must be documented and tested before the problem occurs

	