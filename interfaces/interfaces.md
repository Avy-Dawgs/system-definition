# Interfaces
## Receiver to Companion Computer 
* One directional
* UART 115200 baud, 8 data bits, 1 stop bit
* LSB first
* 16.8 fixed point dBFS power value
* New power reading at about 160 Hz 
## Companion Computer and Base Station
* Via MAVLink broadcast (by passing through flight controller)
* Bidirectional 
* UART
* TUNNEL message to transmit victim locations
* Companion computer will "listen" for messages that it cares about such as position 
	* May be able to assign an update frequency for particular messages
### TUNNEL messages 
* May have to use 0 as sysid for broadcast
#### Payload Values

| Name                   | Payload Value | Args           |
| ---------------------- | ------------- | -------------- |
| Victim Location Local  |               | x, y, z, rssi  |
| Victim Location Global |               | lat, lng, rssi |
## Base Station and ArduPilot Flight Computer
* Bidirectional 
##
