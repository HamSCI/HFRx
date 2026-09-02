---
layout: page
title: Antenna
permalink: /antenna/
---

## Introduction
{:.no_toc}

This page contains deployment protocols. 


## Table of Contents 
{:.no_toc}
* TOC
{:toc}

# Connecting to the Antenna

The current standard antenna selection for the PSWS HRFx is the DX Engineering Receive Short Element Active Vertical Antenn [RSEAV-1](https://www.dxengineering.com/parts/dxe-rseav-1). 

This antenna offer low noise reception from 40 kHz to 30 MHz. The provided three-section 8.5 ft. (2.6m) aluminum tubing whip antenna connected to the internal DXE-AVA-3 Active Matching-amplifier Unit provide significantly better weak signal reception than other active receive antennas and full-size transmit-capable antennas, with reduced noise and lower spurious signal interference. 

<img width="540" height="960" alt="image" src="https://github.com/user-attachments/assets/c646925b-6bad-4518-9c99-8c716e1db97f" />

Normally this antenna is provided on a backplane mounted directly on a 6' copper ground rod (not provided). This exposes the antenna and the active matching-amplifier unit to the elements. While the RSEAV-1's AVA-3 enclosure box itself is weather-resistant, the extra step of enclosing the unit in a suitable weatherproof box ensures that both the RG-6 RF coax and 12VDC power connections are protected from adverse weather, further insuring the dependable performance of the HFRx PSWS.

<img width="540" height="960" alt="image" src="https://github.com/user-attachments/assets/ed3db4a9-3d3a-499e-8583-c4e8a41b71c8" />

While it allows for one cable to be used for both the RF and the DC, since HamSCI wants to study the received transmissions, we want to minimize the signal's noise as much as possible. To do so, we will use a separate cable to supply the antenna it's power-- this requires a simple internal adjustment to the antenna (moving a jumper), as described on the **sixth and seventh page**s in the the RSEAV-1 [manual](https://static.dxengineering.com/global/images/instructions/dxe-rseav-1fvi.pdf?_gl=1*gvjbi2*_gcl_aw*R0NMLjE3ODEyNzM4NDkuRUFJYUlRb2JDaE1JMGVibS1PNkJsUU1WNDBUX0FSM0ZCemZBRUFBWUFTQUFFZ0tyOF9EX0J3RQ..*_gcl_au*MzIxODM4MDkuMTc3OTgyNDIzMS4xMDIyNjczNzQyLjE3ODEyNzM4ODcuMTc4MTI3Mzg4Nw..*_ga*MTU2MjkyMTYwNy4xNzc5ODI0MjMx*_ga_NZB590FMHY*czE3ODI0OTA0MzkkbzQkZzAkdDE3ODI0OTA0NDkkajUwJGwwJGgw). The manual also includes further assembly instructions.

Then, to power the antenna, connect the Jameco power supply to the F-Type Female to RCA Female Adapter, and then to the Female to RCA Male Power Adapter Cable, which will then connect to the antenna.

<img width="540" height="960" alt="image" src="https://github.com/user-attachments/assets/0d3e73a9-dcb8-4f74-bd75-c6ccab19c0ee" />



<img width="1707" height="960" alt="image" src="https://github.com/user-attachments/assets/cb283d4b-d0cf-437b-a40e-7a77cff32dce" />
