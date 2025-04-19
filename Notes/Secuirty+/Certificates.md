## Digital certificates
- A public key certificate
	- Binds a public key with a digital signature
	- And other details about the key holder
- A digital signature adds trust
	- PKI uses Certificate Authorities for additional trust
	- Web of Trust adds other users for additional trust
- Certificates creation can be built into the OS
	- Part of Windows Domain services
	- Many 3rd-party options
## What is a digital certificate?
- X.509
	- Standard format
- Certificate details
	- Serial number
	- Version
	- Signature Algorithm
	- Issuer
	- Name of the cert holder
	- Public key
	- Extensions
	- And more...
## Root of trust
- Everything associated with IT security requires trust
	- A foundational characteristic
- How to build trust from something unknown?
	- Someone/something trustworthy provides their approval
- Refer to the root of trust
	- An inherently trusted component
	- Hardware, software, firmware, or other component
	- Hardware security module (HSM), Secure Enclave, Certificate Authority, etc.
## Certificate Authorities
- You connect to a random website
	- Do you trust it?
- Need a good way to trust an unknown entity
	- Use a trusted third-party
	- An authority
- Certificate Authority (CA) has digitally signed the website certificate
	- You trust the CA, therefore you trust the website
	- Real-time verification
## Third-party certificate authorities
- Built-in to your browser
	- Any browser
- Purchase your web site certificate
	- It will be trusted by everyone's browser
- CA is responsible for vetting the request
	- They will confirm the certificate owner
	- Additional verification information may be required by the CA
## Certificate signing requests
- Create a key pair, then send the public key to the CA to be signed
	- A certificate signing request (CSR)
- The CA validates the request
	- Confirms DNS emails and website ownership
- CA digitally signs the cert
	- Returns to the applicant
## Private certificate authorities
- You are your own CA
	- Build it in-house
	- Your devices must trust the internal CA
- Needed for medium-to-large organizations
	- Many web servers and privacy requirements
- Implement as part of your overall computing strategy
	- Windows Certificate Services, OpenCA
## Self-signed certificates
- Internal certificates don't need to be signed by a public CA
	- Your company is the only one going to use it
	- No need to purchase trust for devices that already trust you
- Build your own CA
	- Issue your own certificates signed by your own CA
- Install the CA certificate/trusted chain on all devices
	- They'll now trust any certificates signed by your internal CA
	- Works exactly like a certificate you purchased
## Wildcard certificates
- Subject Alternative Name (SAN)
	- Extension to an X.509 certificate
	- Lists additional identification information
	- Allows a certificate to support many different domains
- Wildcard domain
	- Certificates are based on the name of the server
	- A wildcard domain will apply to all server names in a domain
## Key revocation
- Certificate Revocation List (CRL)
	- Maintained by the Certificate Authority (CA)
	- Can contain many revocations in a large file
- Many different reasons
	- Changes all the time
- April 2014 - CVE-2014-0160
	- Heartbleed
	- OpenSSL flaw put the private key of affected web servers at risk
	- OpenSSL was patched, every web server certificate was replaced
	- Older certificates were moved to the CRL
## OCSP stapling
- Online Certificate Status Protocol
	- Provides scalability for OCSP checks
- The CA is responsible for responding to all client OCSP requests
	- This may not scale well
- Instead, have the certificate holder verify their own status
	- Status information is stored on the certificate holder's server
- OCSP status is "stapled" into the SSL/TLS handshake
	- Digitally signed by the CA
## Getting revocation details to the browser
- OCSP (Online Certificate Status Protocol)
	- The browser can check certificate revocation
- Messages usually sent to an OCSP responder via HTTP
	- Easy to support over Internet links
	- More efficient than downloading a CRL
- Not all browsers/apps support OCSP
	- Early Internet Explorer versions did not support OCSP
	- Some support OCSP, but don't bother checking