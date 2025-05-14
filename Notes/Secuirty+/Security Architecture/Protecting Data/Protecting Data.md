## Geographic restrictions
- Network locations
	- Identify based on IP subnet
	- Can be difficult with mobile devices
- Geolocation - determine a user's location
	- GPS - mobile devices, very accurate
	- 802.11 wireless, less accurate
	- IP address, not very accurate
- Geofencing
	- Automatically allow or restrict access when the user is in a particular location
	- Don't allow this app to run unless you're near the office
## Protecting data
- A primary job task
	- An organization is out of business without data
- Data is everywhere
	- On a storage drive, on the network (private or public), in a CPU
- Protecting the data
	- Encryption, security policies
- Data permissions
	- Not everyone has the same access
## Encryption
- Encode information into unreadable data
	- Original information is plaintext
	- Encrypted form is ciphertext
- This is a two-way street
	- Convert between one and the other
	- If you have the proper key
- Confusion
	- The encrypted data is drastically different than the plaintext
## Hashing
- Represent data as a short string of text
	- A message digest, fingerprint
- One-way trip
	- Impossible to recover the original message from the digest
	- Used to store passwords/confidentiality
- Verify ta downloaded document is the same as the original
	- Integrity
- Can be a digital signature
	- Authentication, non-repudiation, and integrity
- Will not have a collision (hopefully)
	- Different messages will not have the same hash
## A hashing example
- SHA256 hash
	- 256 bits/64 hexadecimal characters
- My name is Professor Messer
	- SHA256 hash: 
		`19da9a2e26f3bff67f0522f962851c42542b8659333ac53397c8d65aa7a3f871`
- My name is Professor Messer!
	- SHA256 hash:
	   `54381cae1eea10892d81c8688d06d1928b4ee8495061a792864f83092b033aea`
## Obfuscation
- Obfuscate
	- Make something normally understandable very difficult to understand
- Take a perfectly readable code and turn it into nonsense
	- The developer keeps the readable code and gives you the chicken scratch
	- Both sets of code perform exactly the same way
- Helps prevent the search for security holes
	- Makes it more difficult to figure out what's happening
- Example of code obfuscation
		`console.log("Hello World!")`
		Obfuscation output:
		```function _0x5a23(_0x626a46,_0x13fefb){var _0x31eb8a=_0x31eb();return _0x5a23=function(_0x5a234b,_0x1d1948){_0x5a234b=_0x5a234b-0x1a0;var _0x91a7fd=_0x31eb8a[_0x5a234b];return _0x91a7fd;},_0x5a23(_0x626a46,_0x13fefb);}var _0x22481b=_0x5a23;function _0x31eb(){var _0x51007c=['9215352pKDWSz','Hello\x20World!','2262939TDDpAo','8842664IFRUWL','30XzgFsW','2hKyduG','110670THoJJN','6109915UNXVJm','2140194AcGobC','465920OdHyox'];_0x31eb=function(){return _0x51007c;};return _0x31eb();}(function(_0x4db060,_0x346223){var _0x317c91=_0x5a23,_0x43f38f=_0x4db060();while(!![]){try{var _0x41aa21=-parseInt(_0x317c91(0x1a6))/0x1*(-parseInt(_0x317c91(0x1a5))/0x2)+parseInt(_0x317c91(0x1a2))/0x3+parseInt(_0x317c91(0x1a9))/0x4*(parseInt(_0x317c91(0x1a4))/0x5)+parseInt(_0x317c91(0x1a8))/0x6+parseInt(_0x317c91(0x1a7))/0x7+-parseInt(_0x317c91(0x1a3))/0x8+-parseInt(_0x317c91(0x1a0))/0x9;if(_0x41aa21===_0x346223)break;else _0x43f38f['push'](_0x43f38f['shift']());}catch(_0x1448be){_0x43f38f['push'](_0x43f38f['shift']());}}}(_0x31eb,0xa2252),console['log'](_0x22481b(0x1a1)));```
	- Running the above obfuscated code will still log "Hello World!" to the console
## Masking
- A type of obfuscation
	- Hide some of the original data
- Protects PII
	- And other sensitive data
		- ex/ Receipts only showing the last 4 digits of your bank card 
- May only be hidden from view
	- The data may still be intact in storage
	- Control the view based on permissions
- Many different techniques
	- Substituting, shuffling, encrypting, masking out, etc.
## Tokenization
- Replace sensitive data with a non-sensitive placeholder
	- SSN 266-12-1112 is now 691-61-8359
- Common with credit card processing
	- Use a temporary token during payment
	- An attacker capturing the card numbers can't use them later
- This isn't encryption or hashing
	- The original data and token aren't mathematically related
	- No encryption overhead
- How it works:
	- User registers a credit card on their mobile phone: 4112 5478 9967 0421
	- Card is registered with the token service in the server
	- Remote Token Service Server receives credit card number, it then provides a token instead: 4545 \*\*\*\* \*\*\*\* 5678
	- When the phone is used during checkout it will use one of those tokens to pay. The token is sent to the Merchant Payment Processing Server
	- The Merchant Payment Processing Server sends that token to the Remote Token Server to verify. The server validates the token and can be used to purchase products at that store
## Segmentation
- Many organizations use a single data source
	- One large database
- One breach puts all of the data at risk
	- You're making it easy for the attacker
- Separate the data
	- Store it in different locations
- Sensitive data should have stronger security
	- The mist sensitive data should be the most secure
## Permission restrictions
- Control access to an account
	- It's more than just a username and password
	- Determine what policies are best for an organization
- The authentication process
	- Password policies
	- Authentication factor policies
	- Other considerations
- Permissions after login
	- Another line of defense
	- Prevent unauthorized access