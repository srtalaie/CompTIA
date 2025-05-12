## Port security
- We've created many authentication methods through the years
	- A network administrator has many choices
- Use a username and password is a type of port security
- Commonly used on wireless networks
	- Also works on wired networks
## EAP (Extensible Authentication Protocol)
- An authentication framework
- Many different ways to authenticate based on RFC standards
	- Manufacturers can build their own EAP methods
- EAP integrates with 802.1X
	- Prevents access to the network until the authentication succeeds
## IEEE 802.1X
- IEE 8021X
	- Port-based Network Access Control (NAC)
	- You don't get access to the network until you authenticate
- EAP integrates with 802.1X
	- Extensible Authentication Protocol
	- 802.1X prevents access to the network until authentication succeeds
- Used in conjunction with an authentication database
	- RADIUS, LDAP, TACAS+, Kerberos, etc.
## IEEE 802.1X and EAP
- Supplicant - The client or end user
- Authenticator - The device that provides access (switch or access point)
- Authentication server - Validates the client credentials (existing active directory database for example)
- How this works:
	- When the supplicant tries to access the network at first there is no authentication and the authenticator will not grant access until authentication is complete
	- The authenticator sends a message back asking for login credentials called an EAP-request
	- Supplicant provides an EAP-response with the name of the device trying to connect to the network
	- The authenticator passes the response to the authentication server and if the authentication server is accepting logins it will send back a message asking for details to complete authentication
	- The authenticator passes this message along to the supplicant
	- The supplicant then provides the login credentials to the authenticator
	- The authenticator passes them along to the authentication server to see if they are correct
	- If they match the server replies successful login and lets the authenticator provide the supplicant access to the network