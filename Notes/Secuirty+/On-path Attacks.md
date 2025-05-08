## On-path network attack
- How can an attacker watch without you knowing?
	- Formerly known as man-in-the-middle
- Attacker redirects your traffic
	- Then passes it on to the destination
	- You never know your traffic was redirected
- ARP poisoning
	- On-path attack on the local IP subnet
	- ARP has no security
## ARP poisoning (spoofing)
- How it works
	- You have a laptop with IP: 192.168.1.9 and MAC ending with :38:d5
	- A router with IP 192.168.1.1 and MAC ending with :bb:fe
	- When the laptop first connects to the network it doesn't know the hardware address, only the IP address of the router. It's the ARP that resolves the MAC address from the IP address
	- First the laptops sends out a broadcast across the network looking for the IP of the router. If you are this device please send the MAC address
	- The router sees the broadcast and returns the MAC address as its response
	- When the laptop receives the ARP reply it saves it in its cache. Attributing the IP address with the router's MAC address
	- Now we have an attacker with IP 192.168.1.14 and MAC ending with :ee:ff
	- The attacker sends a response to the laptop saying that **IT** is the router and gives the laptop its MAC address
	- Because ARP has no authentication or security it will override its ARP cache with the attackers MAC
	- Now when the laptop wants to talk to the router or vice versa it will send all of its info through the attackers computer
	- The attacker can monitor traffic, modify info passed between the devices or cut off the network all together
## On-path browser attack
- What if the middleman was on the same computer as the victim
	- Malware/Trojan does all of the proxy work
	- Formerly known as man-in-the-browser
- Huge advantages for the attackers
	- Relatively easy to proxy encrypted traffic
	- Everything looks normal to the victim
- The malware in your browser waits for you to login to your bank and cleans you out
