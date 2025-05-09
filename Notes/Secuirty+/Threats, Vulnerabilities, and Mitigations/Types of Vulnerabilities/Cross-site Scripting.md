## Cross-site scripting
- XSS
	- A type of web security vulnerability that allows an attacker to inject malicious code into a trusted website or application. This code can then be executed by other users of the site, potentially leading to various attacks like stealing user data or redirecting users to malicious sites
- Originally called cross-site because of browser security flaws
	- Information from one site could be shared with another
- One of the most common web app vulnerabilities
	- Takes advantage of the trust a user has for a site
	- Complex and varied
- XSS commonly uses JavaScript
## How it works
- An attacker sends a link containing a malicious script inside of it (via email, text, etc.)
- Victim clicks on the link and it takes them to a legitimate site
- Legitimate site loads in the victim's browser. Malicious script is also executed
- Malicious script sends victim's data (session cookies, etc.) to the attacker
## Non-persistent (reflected) XSS attack
- Web site allows scripts to run in user input
	- Search box is a common source
- Attacker emails a link that takes advantage of this vulnerability
	- Runs a script that sends credentials/session IDS/cookies to the attacker
- Script embedded in URL executes in the victim's browser
	- As if it came from the server
- Attacker uses credentials/session IDS/cookies to steal victim's information without their knowledge
## Persistent (stored) XSS attack
- Attacker posts a message to a social network
	- Includes the malicious payload
- It's now "persistent"
	- Everyone gets the payload
- No specific target
	- All viewers to the page are vulnerable
- For social networking this can spread quickly
	- Everyone who views the message can have it posted to their page
	- When someone else can view it and propagate it further
## Hacking a Subaru
- June 2017, Aaron Guzman
	- Security Researcher
- When authenticating with Subaru, users get a token
	- This token never expires (bad!)
- A valid token allowed any service request
	- Even adding your email address to someone else's account
	- Now you have full access to someone else's car
- Web front-end included an XSS vulnerability
	- A user clicks a malicious link, and you have their token
## Protecting against XSS
- Be careful when clicking untrusted links
	- Never blindly click in your email inbox
- Consider disabling JavaScript
	- Or control with an extension
	- This offers limited protection
- Keep your browser and applications updated
	- Avoid the nasty browser vulnerabilities
- Validate input
	- Don't allow users to add their own scripts to an input field
