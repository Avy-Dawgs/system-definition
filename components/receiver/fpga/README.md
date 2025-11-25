# FPGA

## Firmware Diagram
![](../../../.diagrams/receiver-firmware.drawio.svg)
## Description 
The FPGA will be responsible for converting a stream of ADC samples into 457 kHz power values. 
Additionally, the firmware will also control the gain of the PGAs.
The FPGA board is the Digilent CMOD S7.

## Inputs 
| Name     | Width |
| -------- | ----- |
| ADC MISO | 1     |

## Outputs 
| Name             | Width |
| ---------------- | ----- |
| ADC SCK          | 1     | 
| ADC CS_N         | 1     |
| PGA MOSI         | 1     |
| PGA SCK          | 1     | 
| PGA CS_N         | 1     | 
| HGA Bypass       | 1     |
| UART TX          | 1     |

## Firmware Components
* Low-pass filter to remove DC offset
* Narrowband digital down conversion to convert to baseband with a very narrow bandwidth
* Gain control state machine to keep incoming signal within ADC range
