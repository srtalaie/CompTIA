## Code injection
- Code Injection
	- Adding your own information into a data stream
- Enabled because of bad programming
	- The application should properly handle input and output
- So many different data types
	- HTML, SQL, XML, LDAP, etc.
## SQL injection
- SQL - Structured Query Language
	- The most common relational database management system language
- SQL injection (SQLi)
	- Put your own SQL requests into an existing application
	- Your application shouldn't allow this
- Can be often executed in a web browser
	- Inject in a form or field
## Handling a SQL injection
- An example of website code:
		```"SELECT * FROM users WHERE name = '" + userName + "'";```
- How this looks to the SQL database:
		```"SELECT * FROM users WHERE name = 'Professor'";```
- Add more information to the query:
		```"SELECT * FROM users WHERE name = 'Professor' OR '1' = '1'";```
	- This will ask for everything in the database w/ ```OR '1' = '1'``` is the injected code
- This could be very bad
	- View all database information, delete database information, add users, denial of service, etc.4


Examples of SQL injections can be found at [Web Goat](https://owasp.org/www-project-webgoat/)
