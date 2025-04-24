## Finding malware
- Malware runs in memory
	- Memory forensics can find the malicious code
- Memory contains running processes
	- DLLs (Dynamic Link Libraries) - a collection of small programs that larger programs can load when needed to complete specific tasks. The small program, called a DLL file, contains instructions that help the larger program handle what may not be a core function of the original program
	- Threads -a basic unit of execution within a process. It's a sequence of instructions that can be managed independently by the operating system
	- Buffers - memory used as temporary location for data in a program
	- Memory management functions - a set of procedures within an operating system that handle the allocation, usage, and deallocation of computer memory
	- And much more
- Malware is hidden somewhere
	- Malware runs in its own process in memory
	- Malware injects itself into a legitimate process
## Memory injection
- Add code into the memory of an existing process
	- Hide malware inside of the process
- Get access to the data in that process
	- And the same rights and permissions
	- Perform a privilege escalation
## DLL injection
- Dynamic-Link Library
	- A windows library containing code and data
	- Many applications can use this library
- Attackers inject a path to a malicious DLL
	- Runs as part of the target process
	- When the process hits the point where the path reference is. It goes outside of disk to the malicious DLL and loads the malicious code into memory. Now the malware is running on that system.
- One of the most popular memory injection methods
	- Relatively easy to implement
