# Companion Computer 
## Description 
Receives a stream of input data from the beacon receiver, and MAVLink messages from the drone's flight controller, 
using this information to determine an approximate location of avalanche beacons. 
This information is relayed back to the base station via a MAVLink message.

## Inputs 
| Name                 | Type   |
| -------------------- | ------ |
| Receiver Data Stream | Serial |
| MAVLink Input        | Serial |

## Outputs 
| Name           | Type   |
| -------------- | ------ |
| MAVLink Output | Serial |

## Software Components 

### Signal Processing 
* Receives data stream from receiver
* Initiates an event or callback every time a pulse is detected
* This component could be switched out with a wifi signal strength measurement to test without a functional receiver

### MAVLink Interface. 
* Listens for commands and messages, initiating an event or callback if necessary
	* example message: local position
	* example command: takeoff
* Sends messages 
	* example: tunnel for beacon location

### Signal Map Data Structure
* Represents the signal strength in finite xy chunks

### Location Finding Algorithm 
* Updates signal map data structure when new signal reading is available 
* Examines the signal map to determine where the "peaks" are, indicating the location of a beacon
