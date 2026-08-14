---
layout: page
title: About
permalink: /about/
mermaid: true
---

## What is a HamSCI HFRx Personal Space Weather Station?

The HFRx HamSCI HF Personal Space Weather Station (PSWS) is a purpose-built instrument. A direct-sampling Software Defined Radio (SDR) system able to simultaneously receive and process the full MF and HF bands - from 0.3 to 30 MHz. Its purpose is to provide important data to the HamSCI Citizen Science Project by monitoring changes in the Earth's ionosphere via receiving, decoding, digitizing and archiving precision radio signals on a 24/7/365 basis.  

The HFRx PSWS incorporates a commercially available RX-888 MkII 16-bit SDR receiver, supplemental filtering, a GPS Disciplined oscillator and an 'Active' HF receive-only antenna. It uses a Linux Ubuntu OS computer to run specialized software to process data received by  for uploading, processing and analysis by the HamSCI Citizen Science Project.   

At the core of the HFRx PSPS is the WSPRDeamon software by Rob Robinette AI6VN, which incorporates Phil Karn's ka9q-radio. This Linux application is designed to allow the HFRx PSWS to operate as a reliable, autonomous scientific data collection instrument for Amateur Radio operators and researchers. Its primary function is to decode WSPR and FST4W spots from one or more Software-Defined Radios (SDRs) and reliably upload these spots to public databases like [wsprnet.org](https://www.wsprnet.org) and [wspr.rocks](https://www.wpsr.rocks) The WSPRDaemon project emphasizes high reliability, advanced features, and scientific data collection going beyond the capabilities of applications like WSJT-X.

Each HFRx PSWS becomes a part of geographically distributed, multi-instrument system for ground-based space environment measurements. Data from each instrument (known as a 'Node') is aggregated with submissions from other HFRx PSWS nodes into a central HamSCI database for space science research. This data is useful for studying the behavior of the ionosphere.

The HFRx PSWS makes two primary types of observations: HF Doppler measurements (measurements of the Doppler shifts of the transmissions of HF WWV government time standard stations and WSPR/FST4W decodes (signal and noise estimates for each WSPR spot, and Doppler shift measurements, when precision frequency references are available).   

Here is a very thorough video that explains the project and the PSWS in detail: [Introduction to the HamSCI PSWS by Gwyn G3ZIL Deployment, Development and Data](https://youtu.be/CAIQzHuQVOQ?si=VF8KUc8So3yxpXWI) - Return here after you've watched the video and continue with the 'Materials' section.   

<img width="1399" height="580" alt="image" src="https://github.com/user-attachments/assets/d8b092b5-aef6-4c5b-937b-6600116442ea" />
