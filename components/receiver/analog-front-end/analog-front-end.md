# Analog Front End
## Diagram 
![](../../../diagrams/receiver-analog-front-end.drawio.svg)

## Description
The analog front end will take a signal from the antenna, filter it, amplify it, and digitize it. 
The signal chain will consist of an LNA, followed by a band pass filter, then two stages of programmable gain amplifiers, and finally the ADC.

## Inputs 
| Name             | Type    | Width        |
| ---------------- | ------- | ------------ |
| PGA Stage 1 Ctrl | Digital | 2 bit        |
| PGA Stage 2 Ctrl | Digital | 2 bit        |
| Antenna Signal   | Analog  | Single Ended |

## Outputs 
| Name     | Type    | Width  |
| -------- | ------- | ------ |
| ADC Data | Digital | 12 bit |

## Components

### LNA 
* Approximately 10dB gain
* As low a noise factor as possible
* High input impedance

### Band Pass Filter 
* Narrow pass band, (ideally close to 160 Hz) centered at 457 kHz 
* Pass band attenuation less than 10 dB

### PGAs
* Series of two with a total max gain of 70 dB (40 dB each)
* Controllable via GPIO

#### First Stage Gain Values
| Ctrl | Gain (dB) |
| ---- | --------- |
| 0b00 | -20       |
| 0b01 | -10       |
| 0b10 | 0         |
| 0b11 | 40        |

#### Second Stage Gain Values
| Ctrl | Gain (dB) |
| ---- | --------- |
| 0b00 | 0         |
| 0b01 | 10        |
| 0b10 | 20        |
| 0b11 | 30        |

### ADC 
* ~10 MSPS 
* 12 bit 
* Parallel interface
