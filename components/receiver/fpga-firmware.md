# FPGA Firmware
## Diagram
![](../../diagrams/receiver-firmware.drawio.svg)
## Description 
The firmware will be responsible for converting a stream of ADC samples into 457 kHz power values. Additionally, the firmware will also control the gain of the PGAs.
## Inputs 

| Name     | Width |
| -------- | ----- |
| ADC Data | 12    |
## Outputs 

| Name             | Width |
| ---------------- | ----- |
| UART RSSI        | 1     |
| PGA Stage 1 Ctrl | 2     |
| PGA Stage 2 Ctrl | 2     |
## Components
* Simple low-pass filter to remove DC 
	* Can be disabled to prevent updates to internal state
* Goertzel algorithm to computer power at 457 kHz  
	* Is explicitly started to prevent processing of samples during certain periods
* Leading one finder + mantissa LUT to convert to dB 
* Control block for amplifier gain control 
	* Waits for some settle time after changing gain before resuming processing
