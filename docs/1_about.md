---
layout: page
title: About
permalink: /about/
mermaid: true
---

## What is a HamSCI HFRx Personal Space Weather Station?

The HFRx HamSCI HF Personal Space Weather Station (PSWS) is a purpose-built built, direct-sampling Software Defined Radio (SDR) system able to simultaneously receive and process the full MF and HF bands - from 0.3 to 30 MHz. The PSWS incorporates a commercially available RX-888 MkII 16-bit SDR receiver with supplemental filtering, a GPS Disciplined oscillator and an 'Active' HF receive-only antenna. It uses a Linux Ubuntu computer to run specialized software to process data received by the PSWS for processing and analysis by the HamSCI Citizen Science Project. 

At the core of the PSPS is the WSPRDeamon software by Rob Robinette AI6VN, which incorporates Phil Karn's ka9q-radio. This Linux application is designed to allow a PSWS to operate as a reliable, autonomous appliance for Amateur Radio operators and researchers. Its primary function is to decode WSPR and FST4W spots from one or more Software-Defined Radios (SDRs) - including the PSWS's RX888 and reliably upload these spots to public databases like [wsprnet.org](https://www.wsprnet.org) and [wspr.rocks](https://www.wpsr.rocks) The WSPRDaemon project emphasizes high reliability, advanced features, and scientific data collection going beyond the capabilities of applications like WSJT-X.

Each PSWS becomes a part of geographically distributed, multi-instrument system for ground-based space environment measurements. Data from this node is aggregated with submissions from other PSWS nodes into a central HamSCI database for space science research. This data is useful for studying the behavior of the ionosphere.

The PSWS makes two primary types of observations: HF Doppler measurements (measurements of the Doppler shifts of the transmissions of HF WWV government time standard stations and WSPR/FST4W decodes (signal and noise estimates for each WSPR spot, and Doppler shift measurements, when precision frequency references are available).   

<img width="986" height="6256" alt="image" src="https://github.com/user-attachments/assets/66a9b369-b5d2-48f6-b652-8e026630b8a3" />


### Modifications to the stock RX-888 SDR for use as a HamSCI HFRx PSWS: 

While the stock RX-888 is a very capable SDR, certain modifications are needed to create a HFRx PSWS. To provide the required timing accuracy necessary, a sampling clock with an accuracy of 10 mHz - which is higher what the RX-888 internal oscillator provides - is required. The Leo Bodnar LB1420 GPSDO provides that accuracy and is connected to the RX-888's circuit board via a special interface. Additionally, the RX-888 SDR has inadequate temperature control which can be addressed by adding a large thermal pad to the bottom of the board. [The RX888 Clock Kit and Thermal Pad ](https://tapr.org/product/rx888-clock-kit-and-thermal-pad/) contains the supplies to make these modifications, and the manual for it is available online [RX888 Clock Kit Manual](https://turnislandsystems.com/wp-content/uploads/2024/05/RX888-Kit-2.pdf). More information in the Build section.
