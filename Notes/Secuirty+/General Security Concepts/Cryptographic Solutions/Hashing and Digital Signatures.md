## Hashes
- Represent data as a short string of text
	- A message digest, a fingerprint
- One-way trip
	- Impossible to recover the original message from the digest
	- Used to store passwords/confidentiality
- Verify a downloaded document is the same as the original
	- Integrity
- Can be a digital signature
	- Authentication, non-repudiation, and integrity
## A hash example
- SHA256 hash
	- 256 bits/64 hexadecimal characters
- ex/ My name is Professor Messer.
	- Hash: 19da9a2e26f3bff67f0522f962851c42542b8659333ac53397c8d65aa7a3f871
- ex/ My name is Professor Messer!
	- Hash: 54381cae1eea10892d81c8688d06d1928b4ee8495061a792864f83092b033aea
- One minor change to the text creates a completely different hash
## Collision
- Hash functions
	- Take an input of any size
	- Create a fixed size string
	- Message digest, checksum
- The hash should be unique
	- Different inputs should never create the same hash
	- If they do, it's a collision
- MD5 has a collision problem
	- Found in 1996
	- Don't use MD5 for anything important
## Practical hashing
- Verify a downloaded file
	- Hashes may be provided on the download site
	- Compare the downloaded file hash with the posted hash value
- Password Storage
	- Instead of storing the password, store a salted hash
	- Compare hashes during the authentication process
	- Nobody ever knows your actual password
## Adding some salt
- Salt
	- Random data added to a password when hashing
- Every user gets their own random salt
	- The salt is commonly stored with the password
- Rainbow tables won't work with salted hashes
	- Technique to reverse engineer hashes
	- Pre-compiled set of every possible input and a series of hashes associated with that input
	- Additional random value added to the original password
- This slows things down the brute force process
	- It doesn't completely stop the reverse engineering
## Salting the hash
- Each user gets a different random hash
	- The same password creates a different hash
	- Ex/ Password: dragon
		- W/o salt: a9c43be948c5cabd56ef2bacffb77cdaa5eec49dd5eb0cc4129cf3eda5f0e74c
		- w/ salt: 744ea9bbb02fe74c84967b6bcf10e0d5db5c5b917b1ff40af01a5f82e0128b5c
## Digital signatures
- Prove the message was not changed
	- Integrity
- Prove the source of the message
	- Authentication
- Make sure the signature isn't fake
	- Non-repudiation
- Sign with the private key
	- The message doesn't need to be encrypted
	- Nobody else can sign this (obviously)
- Verify with the public key
	- Any change in the message will invalidate the signature
## Creating a digital signature
- Plaintext message from the sender is sent through a hashing algorithm and a hash of the plaintext is created
- The hash that is created is then encrypted with the sender's private key. This combination is the digital signature
- Plaintext is sent along with the digital signature
- Recipient  gets the plaintext and the digital signature
- To verify the message received is the message sent the digital signature is decrypted using the sender's public key. The results is a hash of the plaintext.
- A hashing algorithm is preformed on the plaintext message and then the result is compared with the decrypted hash. If the results match then we know the digital signature is verified.