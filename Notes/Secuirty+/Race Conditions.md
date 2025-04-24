## Race condition
- A programming conundrum
	- Sometimes, things happen at the same time
	- This can be bad if you've not planned for it
- Time-of-check to time-of-use (TOCTOU)
	- Check the system
	- When do you use the results of your last check?
	- Something might happen between the check and the use
## Race condition example
- Developer of this program assumes deposits to accounts are immediate, while withdrawals are not
- User 1 and User 2 are moving money between two accounts. Account A has $100. Account B has $100
- User 1 transfer $50 from A to B. User 1 checks balance. Balance shows A and B still have $100
- While that occurs User 2 transfers $50 from A to B. User 2 checks balance. Balance shows A and B still have $100
- User 1 then initiates the transfer. A has $100. B now shows $150
- User 2 initiates the same action. A shows $100. B now shows $200 because deposits show immediately
- Now User 1 Removes $50 from  A. A now shows $50 while B shows $200 for User 1
- User 2 performs the same action. A now shows $50 while B shows $200 for User 2 because withdrawals are not shown immediately
- This final step is where the race condition occurs. The accounts are not immediately updated. The final ending account value for User 2 is A has $50 and B has $200. In reality A should have $0
## Race conditions can cause big problems
- January 2004 - Mars rover "Spirit"
	- Reboot when a problem is identified
	- Problem is with the file system, so reboot because of the file system problem
	- Reboot loop was the result
- Pwn2Own Vancouver 2023 - Tesla Model 3
	- TOCTOU attack against the Tesla infotainment using Bluetooth
	- Elevated privileges to root
	- Earned $100,000 US prize and they keep the Tesla