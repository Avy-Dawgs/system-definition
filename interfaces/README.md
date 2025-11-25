# Interfaces

## Receiver to Companion Computer 
* One directional
* UART 115200 baud, 8 data bits, 1 stop bit
* LSB first

## Companion Computer and Base Station
* Bidirectional 
* UART 115200 baud
* Routed through flight controller 
* Uses MAVLink protocol (see ```mavlink``` folder for details)
