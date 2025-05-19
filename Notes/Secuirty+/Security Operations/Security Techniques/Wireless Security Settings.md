## Securing a wireless network
- An organization's wireless network can contain confidential information
	- Not everyone is allowed access
- Authenticate the users before granting access
	- Who gets access to the wireless network?
	- Username, password, multi-factor authentication
- Ensure that all communication is confidential
	- Encrypt the wireless data
- Verify the integrity of all communication
	- The received data should be identical to the original sent data
	- A message integrity check (MIC)
## The WPA2 PSK problem
- WPA2 has a PSK (Pre-shared Key) brute-force problem
	- Listen to the four-way handshake
		- Some methods can derive the PSK hash without the handshake
	- Capture the hash
- With the hash, attackers can brute force the pre-shared key (PSK)
- This has become easier as technology improves
	- A weak PSK is easier to brute force
	- GPU processing speeds
	- Cloud-based password cracking
- Once you have the PSK, you have everyone's wireless key
	- There's no forward secrecy
## WPA3 and GCMP
- Wi-Fi Protected Access 3 (WPA3)
	- Introduced in 2018
- GCMP block cipher mode
	- Galois/Counter Mode Protocol
	- A stronger encryption than WPA2
- GCMP security services
	- Data confidentiality with AES
	- Message Integrity Check (MIC) with Galois Message Authentication Code (GMAC)
## SAE
- WPA3 changes the PSK authentication process
	- Includes mutual authentication
	- Creates a shared session key without sending that key across the network
	- No more four-way handshakes, no hashes no brute-force attacks
- Simultaneous Authentication of Equals (SAE)
	- A Diffie-Hellman derived key exchange with an authentication component
	- Everyone uses a different session key, even with the same PSK
	- An IEEE standard - the dragonfly handshake
## Wireless authentication methods
- Gain access to a wireless network
	- Mobile users
	- Temporary users
- Credentials
	- Shared password/pre-shared key (PSK)
	- Centralized authentication (802.1X)
- Configuration
	- Part of the wireless network connection
	- Prompted during the connection process
## Wireless security modes
- Configure the authentication on your wireless access point/wireless router
- Open system
	- No authentication password is required
- WPA3-Personal/WPA3-PSK
	- WPA2 or WPA3 with a pre-shared key
	- Everyone uses the same 256-bit key
- WPA3-Enetrprise/WPA3-802.1X
	- Authenticates users individually with an authentication server (i.e. RADIUS)
## AAA Framework
- Identification
	- This is who you claim to be
	- Usually a username
- Authentication
	- Prove you are who you say you are
	- Password and other authentication factors
- Authorization
	- Based on your identification and authentication, what do you have access to?
- Accounting
	- Resources used: Login time, data sent/received, logout time
## Gaining access
- Logging in from home you are prompted for a username/password from a Firewall/VPN Concentrator
- That info is sent to a AAA server for authentication
- If approved you get access to the rest of the network
## RADIUS (Remote Authentication Dial-in User Service)
- One of the more common AAA protocols
	- Supported on a wide variety of platforms and devices
	- Not just for dial-in
- Centralize authentication for users
	- Routers, switches, firewalls
	- Server authentication
	- Remote VPN access
	- 802.1X network access
- RADIUS services available on almost any server operating system
## IEEE 802.1X
- IEEE 802.1X
	- Port-based Network Access Control (NAC)
	- You don't get access to the network until you authenticate
- Used in conjunction with an access database
	- RADIUS, LDAP, TACACS+
## EAP
- Extensible Authentication Protocol (EAP)
	- Authentication framework
- Many different ways to authenticate based on RFC standards
	- Manufacturers can build their own EAP methods
- EAP integrates with 802.1X
	- Prevent access to the network until authentication succeeds
## IEEE 802.1X and EAP
- Supplicant - the client
- Authenticator - the device that provides access
- Authentication server - validates the client credentials
- How it works
	- When you first try to access the network the authenticator will let the supplicant know they are not authorized to access the network. It then asks if this is a new connection, if so then provide authorization credentials (EAP-Request)
	- The supplicant provides their name (EAP-Response)
	- Authenticator passes the info to the Authentication server, asking if this is someone they should begin the authorization process with
	- Authentication Server tells the authenticator to continue with the process
	- Authenticator asks supplicant for their credentials
	- Supplicant provides those credentials
	- Authenticator passes the credentials to the authentication server who validates the information
	- Responds with either allowing the supplicant to proceed or denies access based on whether the credentials were found to be correct