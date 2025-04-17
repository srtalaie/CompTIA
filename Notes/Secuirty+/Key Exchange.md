## Key exchange
- A logistical challenge
	- How do you share an encryption key across an insecure medium without physically transferring a key?
- Out-of-band key exchange
	- Don't send the symmetric key over the 'net'
	- Telephone, courier, in-person, etc.
- In-band exchange
	- It's on network
	- Protect the key with additional encryption
	- Use asymmetric encryption to deliver symmetric key
## Real-time encryption/decryption
- There's a need for fast security
	- Without compromising the security part
- Share a symmetric session key using asymmetric encryption
	- Client encrypts a random (symmetric) key with a server's public key
	- The server decrypts this shared key and uses it to encrypt data
	- This is the session key
- Implement session keys carefully
	- Need to be changed often (ephemeral keys)
	- Need to be unpredictable
## Symmetric key from asymmetric keys
- Use public and private key cryptography to create a symmetric key
	- Math is powerful
- Workflow:
	- Start with private keys between two users
	- Combine one private key with the other's public key and vice versa for the other user
	- Both combinations now become the same symmetric keys
	- This is called a key exchange algorithm