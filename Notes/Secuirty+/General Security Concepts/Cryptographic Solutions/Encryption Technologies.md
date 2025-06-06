## Trusted Platform Module (TPM)
- A specification for cryptographic functions
	- Cryptography hardware on a device
- Cryptographic processor
	- Random number generator, key generators
- Persistent memory
	- Unique keys burned in during manufacturing
- Versatile memory
	- Storage keys, hardware configuration information
	- Securely store BitLocker keys
- Password protected
	- No dictionary attacks
## Hardware Security Module (HSM)
- Used in large environments
	- Clusters, redundant power
	- Securely store thousands of cryptographic keys
- High-end cryptographic hardware
	- Plug-in card or separate hardware device that can connect to the HSM and perform very fast cryptographic functions
- Key backup
	- Secure storage in hardware
- Cryptographic accelerators
	- Offload that CPU overhead form other devices
## Key management system
- Services are everywhere
	- On-premises, cloud-based
	- Many different keys for many different services
- Manage all keys from a centralized manager
	- Often provided as third-party software
	- Separate the encryption keys from the data
- All key management from one console
	- Create keys for a specific service or cloud provider (SSL/TLS, SSH, etc.)
	- Rotate keys on regular intervals
	- Log key use and important events
## Keeping data private
- Our data is located in may different places
	- Mobile phones, cloud, laptops, etc.
	- The most private data is often physically closest to us
- Attackers are always finding new techniques
	- It's a race to stay one step ahead
- Our data is changing constantly
	- How do we keep this data protected
## Secure enclave
- A protected area for our secrets
	- Often implemented as a hardware processor
	- Isolated form the main processor
	- Many different technologies and names
- Provides extensive security features
	- Has its own boot ROM
	- Monitors the system boot process
	- True random number generator
	- Real-time memory encryption
	- Root cryptographic keys
	- Performs AES encryption in hardware
	- And more...