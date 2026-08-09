---
layout: page
title: About
permalink: /about/
mermaid: true
---

# What is the HF PSWS Reciever?

The HF PSWS Receiver is a direct-sampling, GPS-disciplined Software Defined Radio (SDR) system able to simultaneously receive and process the full MF and HF bands (from 0.3 to 30 MHz). The instrument uses a commercially available RX-888 MkII 16-bit SDR receiver, with additional filters and a GPSDO interface (described in detail below) custom-designed built, supplied and supported by Turn Island Systems, via project participant Paul Elliott 9WB6CXC). 
To complete the instrument, it requires a computer to run KA9Q-Radio and WSPR-Daemon software, such a Beelink, an external GPSDO, and an antenna.

The receiver makes two primary types of observations: HF Doppler measurements (measurements of the Doppler shifts of the transmissions of HF government time standard stations, such as WWV and CHU) and WSPR/FST4W decodes (signal and noise estimates for each WSPR spot, and Doppler shift measurements, when precision frequency references are available).

# Modifications to the RX-888 SDR: 

Before connecting the RX-888 SDR to anything, there are some necessary modifications to make. We need a sampling clock with an accuracy of 10 mHz, which is higher what the RX-888 internal oscillator provides, so we need to connect the RX-888's circuit board to an external clock. And the RX-888 has poor thermal control which can be addressed by adding a large thermal pad to the bottom of the board. [The RX888 Clock Kit and Thermal Pad ](https://tapr.org/product/rx888-clock-kit-and-thermal-pad/) contains the supplies to make these modifications, and the manual for it is available online [RX888 Clock Kit Manual](https://turnislandsystems.com/wp-content/uploads/2024/05/RX888-Kit-2.pdf).




# Connecting to the Antenna

For the HF receiver, the current standard antenna is the DX Engineering [RSEAV-1](https://www.dxengineering.com/parts/dxe-rseav-1). 

While it allows for one cable to be used for both the RF and the DC, since HamSCI wants to study the received transmissions, we want to minimize the signal's noise as much as possible. To do so, we will use a separate cable to supply the antenna it's power-- this requires a simple internal adjustment to the antenna (moving a jumper), as described on the **sixth and seventh page**s in the the RSEAV-1 [manual](https://static.dxengineering.com/global/images/instructions/dxe-rseav-1fvi.pdf?_gl=1*gvjbi2*_gcl_aw*R0NMLjE3ODEyNzM4NDkuRUFJYUlRb2JDaE1JMGVibS1PNkJsUU1WNDBUX0FSM0ZCemZBRUFBWUFTQUFFZ0tyOF9EX0J3RQ..*_gcl_au*MzIxODM4MDkuMTc3OTgyNDIzMS4xMDIyNjczNzQyLjE3ODEyNzM4ODcuMTc4MTI3Mzg4Nw..*_ga*MTU2MjkyMTYwNy4xNzc5ODI0MjMx*_ga_NZB590FMHY*czE3ODI0OTA0MzkkbzQkZzAkdDE3ODI0OTA0NDkkajUwJGwwJGgw). The manual also includes further assembly instructions.

Then, to power the antenna, connect the Jameco power supply to the F-Type Female to RCA Female Adapter, and then to the Female to RCA Male Power Adapter Cable, which will then connect to the antenna.





