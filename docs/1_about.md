---
layout: page
title: About
permalink: /about/
mermaid: true
---

# What is the HamSCI HF Personal Space Weather Receiver - PSWS?

The HF PSWS Receiver is a specially built direct-sampling Software Defined Radio (SDR) system able to simultaneously receive and process the full MF and HF bands - from 0.3 to 30 MHz. The PSWS uses the commercially available RX-888 MkII 16-bit SDR receiver, with additional filters, a Leo Bodner GPS Disciplined oscillator and a DX Engineering Active HF receive-only antenna. It uses a Linux Ubuntu computer to run KA9Q-Radio and WSPR-Daemon software to process data received by the SDR for processing and analysis by the HamSCI Citizen Science Project.

The receiver makes two primary types of observations: HF Doppler measurements (measurements of the Doppler shifts of the transmissions of HF government time standard stations, such as WWV and CHU) and WSPR/FST4W decodes (signal and noise estimates for each WSPR spot, and Doppler shift measurements, when precision frequency references are available).

# Modifications to the stock RX-888 SDR for use as a HamSCI PSWS: 

While the RX-888 is a very capable SDR, certain improvements and modifications are needed to create a usable PSWS. To provide the required timing accuracy necessary for active PSWS use, a sampling clock with an accuracy of 10 mHz, which is higher what the RX-888 internal oscillator provides is required. The Leo Bodnar LB1420 GPSDO provides that accuracy and is connected to the RX-888's circuit board via a special interface. Additionally, the RX-888 SDR has inadequate temperature control which can be addressed by adding a large thermal pad to the bottom of the board. [The RX888 Clock Kit and Thermal Pad ](https://tapr.org/product/rx888-clock-kit-and-thermal-pad/) contains the supplies to make these modifications, and the manual for it is available online [RX888 Clock Kit Manual](https://turnislandsystems.com/wp-content/uploads/2024/05/RX888-Kit-2.pdf). 



participant Paul Elliott WB6CXC).










