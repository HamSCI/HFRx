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










