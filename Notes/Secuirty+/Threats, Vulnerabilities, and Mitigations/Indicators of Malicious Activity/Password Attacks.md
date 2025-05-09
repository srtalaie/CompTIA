## Plaintext/unencrypted passwords
- Some applications store passwords "in the clear"
	- No encryption. You can read the stored password
	- This is rare, thankfully
- Do not store passwords as plaintext
	- Anyone with access to the password file or database has every credential
- What to do if your application saves passwords as plaintext:
	- Get a better application
## Hashing a password
- Hashes represent data as a fixed-length string of text
	- A message digest, or "fingerprint"
- Will not have collision (hopefully)
	- Different inputs will not have the same hash
- One-way trip
	- Impossible to recover the original message from the digest
	- A common way to store passwords
- SHA-256 hash algorithm
	- Used in many applications
## The password file
- Different across operating systems and applications
	- Different hash algorithms
## Spraying attack
- Try to login with an incorrect password
	- Eventually you're locked out
- There are some common passwords
- Attackers want to guess what your password might be while making sure they don' guess so many times there is a lockout
- Attack an account with the top three (or more) passwords
	- If they don't work, move to the next account
	- No lockouts, no alarms, no alerts
## Brute force
- Try every possible password combination until the hash is matched
- This might take some time
	- A strong hashing algorithm slows things down
- The hacker already has the hash
- Brute force attacks - Online
	- Keep trying the login process
	- Very slow
	- Most accounts will lockout after a number of failed attempts
- Brute force the hash - Offline
	- Obtain a list of users and hashes
	- Calculate a password hash, compare it to a stored hash
	- Large computational resources requirement

