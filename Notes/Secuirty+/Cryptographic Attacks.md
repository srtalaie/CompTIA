## Cryptographic attacks
- You've encrypted data and sent it to another person
	- Is it really secure and how do you know?
- The attacker doesn't have the combination (the key)
	- So they break the safe (the cryptography)
- Finding ways to undo the security
	- There are many potential cryptographic shortcomings
	- The problem is often implementation
## Birthday attack
- In a classroom of 23 students what is the chance of two students sharing a birthday?
	- About 50%
	- For a class of 30 the chance is about 70%
- In the digital world, this is a hash collision
	- A hash collision is the same hash value for two different plaintexts
	- Find a collision through brute force
- The attacker will generate multiple versions of plaintext to match the hashes
	- Protect yourself with a large hash output size
## Collisions
- Hash digests are supposed to be unique
	- Different input data should not create the same hash
- MD5 hash
	- Message Digest Algorithm 5
	- First published in April 1992
	- Collisions identified in 1996
- December 2008: Researchers created CA certificate that appeared legitimate when MD5 is checked
	- Built other certificates that appeared to be legit issued by RapidSSL
## Downgrade attacks
- Instead of using perfectly good encryption, use something that's not so great
	- Force the systems to downgrade their security
- SSL stripping
	- Combines an on-path attack with a downgrade attack
	- Difficult to implement, but big returns for the attacker
	- Attacker must sit in the middle of the conversation
	- Victims browser page isn't encrypted
	- Strips the S away from the HTTPS
## SSL stripping
- Visitor sends GET request to web server, request is made with HTTP instead of HTTPS and starts the process
- The attacker acts as a proxy and passes the request in to the web server unchanged
- Web server recognizes it is unsecure so it sends a status code of 301 Moved to the visitor to use a different web page that uses HTTPS
- The attacker doesn't send the answer to the visitor, instead it sends a different GET request to the web server this time as HTTPS
- Web server returns a status code of 200 Ok back as HTTPS
- Attacker then sends the 200 Ok status to the visitor but sends it over HTTP instead of HTTPS
- Now the visitor sends a POST request with their username and password to login, which is being sent over HTTP so it is not encrypted
- The attacker can read everything in the request and uses the info to log into the web server with the appropriate POST request through HTTPS
- Web server responds with an acknowledgement that it was successful and the attacker passes that back to the visitor
- From now on all communication between the visitor and attacker will be in-the-clear, while all communication between the attacker and the web server will be encrypted