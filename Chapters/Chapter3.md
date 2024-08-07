|[<<< Chapter 2](./Chapter2.md)|[Home](../README.md)|[Chapter 4 >>>](./Chapter4.md)|
|-|-|-|

# Chapter 3: Access related physical channels and signals

## 3.1. Synchronization Signals and Physical Broadcast Channel
|![](../Imgs/Chapter3/SSB.png)|
|:-:|
|Synchronization Signals Block|

- SSB Components: The combination of SS and PBCH forms the SSB in NR.

- Subcarrier Spacing: SSB subcarrier spacing can be:
    - 15 or 30 kHz in FR1
    - 120 or 240 kHz in FR2

- UE Functions via SS Detection: By detecting SS, a UE can:
    - Obtain physical cell identity
    - Achieve downlink synchronization (time and frequency)
    - Acquire timing for PBCH

|![](../Imgs/Chapter3/Primary%20Synchronization%20Signal.png)|
|:-:|
|Primary Synchronization Signal and Secondary Synchronization Signal|


- NR SS Composition:
    - Primary SS (PSS)
    - Secondary SS (SSS)

|![](../Imgs/Chapter3/PSS%20Sequence%20Generation.png)|![](../Imgs/Chapter3/SSS%20Sequence%20Generation.png)|
|:-:|:-:|
|PSS Sequence Generation|SSS Sequence Generation|

- Sequence Modulation:
    - NR PSS: BPSK modulated m-sequence of length 127
    - NR SSS: BPSK modulated Gold sequence of length 127

- Cell Identity Indication: PSS and SSS together indicate up to 1008 different physical cell identities.

- SSB Mapping:
    - Time domain: 4 OFDM symbols
    - Frequency domain: 240 contiguous subcarriers (20 RBs)

- Beamforming and SS Burst Set:
    - Supports beamforming for initial access via SS burst set and beam sweeping
    - Multiple SSBs transmitted in a localized burst set with a periodicity default of 20 ms
    - Up to 64 SSBs can be transmitted in different beams within a 5 ms window

- SSB Timing and Frequency Location:
    - SSB time locations within an SS burst set are determined by numerology and frequency band
    - SSB frequency location configured by higher layer parameters, not necessarily at system bandwidth center
    - Sparser search raster for SSB detection compensates for increased search time due to sparser periodicity.

|[<<< Chapter 2](./Chapter2.md)|[Home](../README.md)|[Chapter 4 >>>](./Chapter4.md)|
|-|-|-|