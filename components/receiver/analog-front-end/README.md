# Analog Front End
## Diagram 
![](../../../.diagrams/receiver-analog-front-end.drawio.svg)

## Description
The analog front end will take a signal from the antenna, filter it, and amplify it.

## Inputs 
| Name             | Type    | Width        |
| ---------------- | ------- | ------------ |
| HGA Bypass       | Digital | 1 bit        |
| PGA Ctrl         | Digital | Serial       |
| Antenna Signal   | Analog  | Single Ended |

## Outputs 
| Name     | Type    | 
| -------- | ------- |
| Amplified Signal | Analog |

## Components

### LNA 
* Approximately 10dB gain
* As low a noise factor as possible
* High input impedance

### Band Pass Filter 
* Narrow pass band, (ideally close to 160 Hz) centered at 457 kHz 
* Pass band attenuation less than 10 dB

### High Gain Amplifier (HGA)
* Gain of about 42 dB 
* Can by bypassed via bidirectional analog muxes on either side 
* Tuned so that it doesn't amplify noise as strongly

### Programmable Gain Amplifier (PGA)
* Opamp in inverting configuration so that it can amplify or attenuate
* Controllable via writing to a digital potentiometer
