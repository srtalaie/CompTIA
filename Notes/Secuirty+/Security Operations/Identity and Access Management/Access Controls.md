## Access control
- Authorization
	- The process of ensuring only authorized rights are exercised
	- Policy enforcement
	- The process of determining rights
	- Policy definition
- User receive rights based on Access Control models
	- Different business needs or mission requirements
## Least privilege
- Rights and permissions should be set to the bare minimum
	- You  only get exactly what's needed to complete your objective
- Al user accounts must be limited
	- Applications should run with minimal privileges
- Don't allow users to run with administrative privileges
	- Limits the scope of malicious behavior
## Mandatory Access Control (MAC)
- The operating system limits the operation on an object
	- Based on security clearance levels
- Every object gets a label
	- Confidential, secret, top secret, etc.
- Labeling of objects uses predefined rules
	- The administrator decides who gets access to what security label
	- Users cannot change these settings
## Discretionary Access Control (DAC)
- The user that creates the data has the control on who can access the data and how they can access that information
- Used in most operating systems
	- A familiar access control model
- You create a spreadsheet
	- As the owner, you control who has access
	- You can modify access at any time
- Very flexible access control
	- Very weak security
## Role-based Access Control (RBAC)
- You have a role in your organization
	- Manager, director team lead, project manager
- Administrators provide access based on the role of the user
	- Rights are gained implicitly instead of explicitly
- In Windows, use Groups to provide role-based access control
	- You are in shipping and receiving, so you can use the shipping software
	- You are the manager, so you can review shipping logs
## Rule-based access control
- Generic term for following rules
	- Conditions other than who you are
- Access is determined through system-enforced rules
	- System administrators, not users
- The rule is associated with the object
	- System checks the ACLs for that object
- Rule example
	- Lab network access is only available between 9 AM and 5 PM
	- Only Chrome browsers may complete this web form
## Attribute-based access control (ABAC)
- Users can have complex relationships to applications and data
	- Access may be based on many different criteria
- ABAC can consider many parameters
	- A "next generation" authorization model
	- Aware of context
- Combine and evaluate multiple parameters
	- Resource information, IP address, time of day, desired action, relationship to the data, etc.
## Time-of-day restrictions
- Almost all security devices include a time-of-day option
	- Restrict access during certain times or days of the week
	- Usually not the only access control
- Can be difficult to implement
	- Especially in a 24-hour environment
- Time-of-day restrictions
	- Train9nig room network is inaccessible between midnight and 6 AM
	- Conference room access is limited after 8 PM
	- R&D databases are only available between 8 Am and 6 PM
