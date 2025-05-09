## Physical isolation
- Devices are physically separate
	- Air gap between Switch A and Switch B
- Must be connected to provide communication
	- Direct connect, or another switch or router
- Web servers in one rack and database servers on another
- Customer A on one switch, customer B on another
	- No opportunity for mixing fata
- Separate devices
	- Multiple units, separate infrastructure
## Logical segmentation with VLANs
- Virtual Local Area Networks (VLANs)
	- Separated logically instead of physically
	- Cannot communicate between VLANs without a Layer 3 device/router
## Software Defined Networking (SDN)
- Networking devices have different functional planes of operation
	- Data, control, and management planes
- Split the functions into separate logical units
	- Extend the functionality and management of a single device
	- Perfectly built for the cloud
- Infrastructure layer/Data plane
	- Process the network frames and packets
	- Forwarding, trunking, encrypting, NAT
- Control layer/Control plane
	- Manages the actions of the data plane
	- Routing tables, session tables, NAT tables
	- Dynamic routing protocol updates
- Application layer/Management plane
	- Configure and manage the device
	- SSH, browser, API
- On a physical switch
	- The number of ports that devices can connect to would be the Infrastructure Layer/Data plane
	- The Control Layer/ Control Plane is what is physically inside of the switch
	- The console inputs and USB inputs are the Application layer/Management plane where you can connect interfaces into the switch
## SDN data flows

| Application Layer/ Management Plane  | ◀ SSh, SNMP, API ▶                | Application Layer/ Management Plane  |
| ------------------------------------ | --------------------------------- | ------------------------------------ |
| **Control Layer/ Control Plane**     | **◀ Dynamic routing protocols ▶** | **Control Layer/ Control Plane**     |
| **Infrastructure Layer/ Data Plane** | **◀ Network Traffic ▶**           | **Infrastructure Layer/ Data Plane** |

