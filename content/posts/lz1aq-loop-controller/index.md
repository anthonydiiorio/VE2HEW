---
title: "LZ1AQ Loop Controller"
date: 2020-10-16T00:00:00-04:00
draft: false
cover:
    image: "controller-1.jpg"
    alt: "Loop Controller"
    relative: true # To use relative path for cover image, used in hugo Page-bundles
    hidden: true
aliases:
    - /2019/12/16/LZ1AQ-Controller.html #Old Jekyll Permalink
---

I wanted to build a fully remotable LZ1AQ Active Antenna controller with off the shelf components. It is very cheap to buy ESP8266 MCUs and multi-channel relay boards online. Why reinvent the wheel? This project can be easily adapted to control remote antenna switches and other devices that can be controlled with relays.

[Download on Github](https://github.com/anthonydiiorio/LZ1AQ-Loop-Controller/)

![](screenshot.png)

![](controller-1.jpg)

![](controller-2.jpg)

![](controller-3.jpg)

## Schematic

![](schematic.png)

## BOM

| Part Number | Description | QTY |
|---|---|---|
| NodeMCU V2 | Microcontroller with ESP8266 | 1 |
| N/A | 4 Channel Relay Module (Active Low) | 1 |
| RM2055M | Hammond Enclosure (50 mm x 140 mm x 190 mm) | 1 |
| HC-6 | Adhesive PCB Supports | 8 |
| BK/HTB-24M-R | Fuse Holder 5mm x 20mm	| 1 |
| 5MF 300-R	| Fuse 300 mA 5mm x 20mm| 10 |
| N/A | DC Connector of your choice | 1 |
| N/A |Panel Mount Micro USB Extension | 1 |
| PGSD-8 | Cable Grommet | 1 |
| N/A | Hookup Wire | Lots |
| N/A | Dupont Jumpers Wires | Lots |

I used PC Motherboard standoffs and screws to rest the power inserter in the enclosure. It is not mounted permanently to allow easy removal of the front panel.

## LZ1AQ Documentation

1 0 0 Loop A  
0 1 0 Loop B  
1 1 0 A + B  
0 0 1 Vertical  

**Note: My code has pin 1 inverted so Loop A is in the Normally Closed position. This allows the loop to function in A mode with no power applied to the MCU or relay board.**

![](http://active-antenna.eu/wp-content/uploads/2014/03/digital-control-aaa-faq.jpg)

[LZ1AQ FAQ: Can the antenna switching be performed digitally?](http://active-antenna.eu/amplifier-kit/faq-aaa-1b/#antenna-swith)