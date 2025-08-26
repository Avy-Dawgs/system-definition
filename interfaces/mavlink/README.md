# MAVLink

## System and Component IDs 
* Drone: system id 1
	* Flight Controller: component id 0?
	* Companion Computer: component id 200?
* Base Station: system id 255 

## Use Case 
* Companion computer uses TUNNEL message to transmit victim locations 
* Companion computer listens for messages that it cares about 
    * may be able to assign update frequency to specific messages

## TUNNEL messages 
* Can use for arbitrary data transfer
* May have to use 0 as target sysid for broadcast
* Uses a payload value to distinguish between different messages

### Payload Values
| Name                   | Payload Value | Args           |
| ---------------------- | ------------- | -------------- |
| Victim Location Local  |               | x, y, z, rssi  |
| Victim Location Global |               | lat, lng, rssi |
