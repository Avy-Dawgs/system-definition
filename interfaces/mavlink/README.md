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

### Payloads 

#### Victim Location Local
* payload value: 1
* payload length: 12
* bytes:
    * 0-3: float x  (m)
    * 4-7: float y  (m)
    * 8-11: float rssi  (dBFS)

#### Victim Location Global
* payload value: 2
* payload length: 12
* bytes:
    * 0-3: float lat  (latitude)
    * 4-7: float lng  (lognitude)
    * 8-11: float rssi  (dBFS)

#### RSSI Location Local
* payload value: 3
* payload length: 12
* bytes:
    * 0-3: float x  (m)
    * 4-7: float y  (m)
    * 8-11: float rssi  (dBFS)

#### RSSI Location Global
* payload value: 4
* payload length: 12
* bytes:
    * 0-3: float lat  (latitude)
    * 4-7: float lng  (lognitude)
    * 8-11: float rssi  (dBFS)
