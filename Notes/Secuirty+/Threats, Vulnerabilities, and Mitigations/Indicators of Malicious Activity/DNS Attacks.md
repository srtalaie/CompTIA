## DNS poisoning
- We rely on our domain name services or our DNS servers to provide us with a conversion between a fully qualified domain name and an IP address
- DNS Poisoning can cause a user to visit an IP address that they did not originally intend on visiting
- Modify the DNS Server
	- Requires some crafty hacking because they are very well protected
- Modify the client host file (located on the clients PC)
	- The host file takes precedent over DNS queries
- Send a fake response to a valid DNS request
	- Requires a redirection of the original request or the resulting response
	- Real-time redirection
	- This is an on-path attack
## DNS spoofing/poisoning
- Attacker on the network w/ IP address for specific domain is 100.100.100.100
- DNS server IP address for specific domain name is 162.159.246.164
- User 1 and User 2 both need to query for that domain name
- A normal query w/o an attacker looks like:
	- User 1 querying the DNS server for that domain name and the DNS server returns the IP address of 162.159.246.164
	- User 1 then fills in that information in their cache and can connect to the domain using the IP address provided
- A query with an attacker on the network that has some how gained access to the DNS server:
	- Attacker connects directly to DNS server and modifies the domain's IP address to 100.100.100.100
	- Meaning if User 2 queries the DNS server for the domain the result will be the attacker's IP address
	- Any subsequent request from User 2 will be directed to the attacker's PC
## Domain hijacking
- Get access to the domain registration and you have control where the traffic flows
	- You don't need to touch the actual servers
	- Determines the DNS names and DNS IP addresses
- Many ways to get into the account
	- Brute force
	- Social engineer the password
	- Gain access to the email address associated with managing the account
	- The usual ways
- Example:
	- Saturday, October 22, 2016, 1 PM
	- Domain name registrations of 36 domains are changed
		- Associated with a Brazilian bank
		- Desktop domains, mobile domains, and more
	- Under hacker control for 6 hours
		- The attackers became the bank
	- Access to 5 million customers, $27 billion in assets
		- Results of the hack have not been publicly released
## URL hijacking
- Redirect users to a site that has a lot of advertising
	- Make money from your mistakes
	- There's a lot of advertising on the internet
	- Attacker gets a new revenue stream opened from the advertising
- Sell the badly spelled domain to the actual owner
	- Attacker has a domain name that is very close to the actual domain name
	- Sell the misspelled domain name to the owner
- Redirect to a competitor
	- Can use that misspelled name to redirect traffic to the owner's competitor
- Phishing site
	- Attacker presents a page that looks exactly like the legitimate site
	- Can gather information unsuspecting users enter into the site
- Infect with a drive-by download
## Types of URL hijacking
- Typosquatting/brandjacking
	- Take advantage of poor spelling by users trying to get to the legitimate domain name
- Outright misspelling
	- ex/ professormesser.com vs. professormessor.com
- A typing error
	- ex/ professormeser.com
- A different phrase
	- ex/ professormessers.com
- Different top-level domain
	- ex/ professormesser.org
