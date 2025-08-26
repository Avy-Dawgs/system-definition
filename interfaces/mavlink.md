# MAVLink
## System and Component IDs 
* Drone: 1
	* Flight Controller: 0?
	* Companion Computer: 200?
* Base Station: 255 
## Message Routing 
## Arbitrary Data Transfer 
* Best option is likely TUNNEL message

## Custom Messages
Define custom messages in ardupilotmega.xml file. 
### ArduPilot
**Untested:** Compile with the custom command in the XML, and the routing code should be able to forward the message.
### QGroundControl 
https://docs.qgroundcontrol.com/master/en/qgc-dev-guide/custom_build/mavlink.html

### MAVSDK
