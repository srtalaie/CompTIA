## Email security challenges
- The protocols used to transfer emails include relatively few security checks
	- Very easy to spoof emails
- Spoofing happens all the time
- The email looks as if it originated from the correct user
	- But did it? How can you tell?
- A reputable sender will configure email validation
	- Publicly available on the sender's DNS server
## Mail gateway
- The gatekeeper
	- Evaluates the source of inbound email messages
	- Blocks it at the gateway before it reaches the user
	- On-site or cloud-based
## Sender Policy Framework (SPF)
- SPF protocol
	- Sender configures a list of all servers authorized to send emails for a domain
- List of authorized mail servers are added to a DNS TXT record
	- Receiving mail servers perform a check to see if incoming mail really did come from an authorized host
## Domain Keys Identified Mail (DKIM)
- A mail server digitally signs all outgoing mail
	- The public key is in the DKIM TXT record
- The signature is validated by the receiving mail servers
	- Not usually seen by the end user
## DMARC
- Domain-based Message Authentication Reporting, and Conformance (DMARC)
	- An extension of SPF and DKIM
- The domain owner decides what receiving email servers should do with emails not validating using SPK and DKIM
	- That policy is written into a DNS TXT record
	- Accept all, send to spam, or reject the email
- Compliance reports are sent to the email administrator
	- The domain owner can see how emails are received