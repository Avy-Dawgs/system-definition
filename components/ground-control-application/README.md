# Base Station 
## Description 
Configures search area and sends mission plan and takeoff command to drone. 
Receives locations of beacons and displays on the map.
This is a modification of an existing application called QGroundControl.

## Customizations of QGroundControl
* Ability to display victim locations on the map which are received from the drone
* Removal of unnecessary UI elements

## Outputs/Inputs 
The only output/input is a bidirectional serial link to a telemetry radio that is connected over USB. 
This allows for sending and receiving of MAVLink messages and commands.
