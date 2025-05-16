## Secure baselines
- The security of an application environment should be well defined
	- all application instances must follow this baseline
	- Firewall settings, patch levels, OS file versions
	- May require constant updates
- Integrity measurements check for the secure baselines
	- These should be performed often
	- Check against well-documented baselines
	- Failure requires an immediate correction
## Establish baselines
- Create a series of baselines
	- Foundational security policies
- Security baselines are often available from the manufacturer
	- Application developer
	- Operating system manufacturer
	- Appliance manufacturer
- Many operating systems have extensive options
	- There are over 3000 group policy settings in Windows 10
	- Only some of those are associated with security
## Deploy baselines
- We now have established detailed security baselines
- Deploy the baselines
	- Usually managed through a centrally administered console
- May require multiple deployment mechanisms
	- Active Directory group policy, MDM, etc.
- Automation is the key
	- Deploy to hundreds or thousands of devices
## Maintain baselines
- Many of these are best practices
	- They rarely change
- Other baselines may require ongoing updates
	- A new vulnerability is discovered
	- An updated application has been deployed
	- A new operating system is installed
- Test and measure to avoid conflicts
	- Some baselines may contradict others
	- Enterprise environments are complex
