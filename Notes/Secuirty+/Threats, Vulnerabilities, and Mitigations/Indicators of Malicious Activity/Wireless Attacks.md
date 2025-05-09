## It started as a normal day
- Surfing along on your wireless network
	- And then you're not
- Wait a bit after reconnection, and then it happens again
	- And again...
- You may not be able to stop it
	- There's (almost) nothing you can do
	- Time to get a long patch cable
- Wireless deauthentication
	- A significant wireless denial of service (DoS) attack
## 802.11 management frames
- 802.11 wireless includes a number of management features
	- Frames that make everything work
		- Used to connect to the network, manage the network, and disconnect from the network when you are done
	- You never see them
- Important for the operation of 802.11 wireless
	- How to find access points, manage QoS, associate/disassociate with an access point, etc.
- Original wireless standards did not add protection for management frames
	- Sent in the clear, no authentication or validation
## Protecting against deauth attacks
- IEEE has already addressed the problem
	- Updates included with 802.11ac
- Some of the important management frames are encrypted
	- Disassociate, deauthenticate, channel switch announcements, etc.
- Not everything is encrypted
	- Beacons, probes, authentication, association
## Radio frequency (RF) jamming
- Denial of Service
	- Prevent wireless communication
- Transmit interfering wireless signals
	- Decrease the signal-to-noise ratio at the receiving device
	- The receiving device can't hear the good signal
- Sometimes it's not intentional
	- Interference, not jamming
	- Microwave oven, fluorescent lights
- Jamming is intentional
	- Someone wants your network to not work
## Wireless jamming
- Many different types
	- Constant, random bits/Constant, legitimate frames
	- Data sent at random times - random data and legitimate frames
	- Reactive jamming - only when someone else tries to communicate
- Needs to be somewhere close
	- Difficult to be effective from a distance
- Time to go fox hunting
	- You'll need the right equipment to hunt down the jam
	- Directional antenna, attenuator