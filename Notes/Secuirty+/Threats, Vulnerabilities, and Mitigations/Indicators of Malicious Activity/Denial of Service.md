## Denial of service
- Force a service to fail
	- Overload the service
- Take advantage of a design failure or vulnerability
	- Keep your systems patched!
- Cause a third-party system to be unavailable
	- Competitive advantage
- Create a smokescreen for some other exploit
	- Precursor to a DNS spoofing attack
- Doesn't have to be complicated
	- Can just be turning the power off
## A "friendly" DoS
- Unintentional DoS'ing
- Network DoS
	- Layer 2 loop without STP
- Bandwidth DoS
	- Downloading multi-gigabyte Linux distributions over a DSL line
- The water line breaks
## Distributed Denial of Service (DDoS)
- Launch an army of computers to bring down a service
	- Use all the bandwidth or resources - traffic spike
- This is why the attackers have botnets
	- Thousands or millions of computers at your command
	- At its peak, Zeus botnet infected over 3.6 million PCs
	- Coordinated attacks
- Asymmetric threats
	- The attacker may have fewer resources than the victim
## DDoS reflection and amplificaton
- Turn your small attack into a big attack
	- Often reflected off another device or service
- An increasingly common network DDoS technique
	- Turn internet services against the victim
- Uses protocols with little (if any) authentication or checks
	- NTP, DNS, ICMP
	- A common example of protocol abuse
## DNS amplification DDoS
- Botnet command send command to botnet to start the DDoS attack
	- I.e. "Preform a query on open DNS resolvers and have the query spoofed so the results are sent to a particular web server"
- Query sent to all of the DNS resolvers from all of the botnet devices
- Results are much larger in comparison to the query sent
- DNS resolvers send the responses to the web server, overwhelming it and causing a DDoS attack