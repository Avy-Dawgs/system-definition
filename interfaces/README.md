# Interfaces

## Receiver to Companion Computer 
* One directional
* UART 115200 baud, 8 data bits, 1 stop bit
* LSB first
* 16.8 fixed point dBFS power value
* New power reading at about 160 Hz 

## Companion Computer and Base Station
* Bidirectional 
* UART
* Routed through ArudPilot flight controller 
* Uses MAVLink protocol (see ```mavlink``` folder for details)
