## 5 Generic functions

### 5.1 Modulation mapper

### 5.2 Sequence generation

#### 5.2.1 Pseudo-random sequence generation

Generic pseudo-random sequences are defined by a length-31 Gold sequence. The output sequence *c(n)* of length *M<sub>PN</sub>* where *n* = 0, 1,... , *M<sub>PN</sub> - 1* is defined by:

*c(n) = (x<sub>1</sub>(n + N<sub>C</sub>) + x<sub>2</sub>(n + N<sub>C</sub>)) mod 2*

x<sub>1</sub>(n + 31) = (x<sub>1</sub>(n + 3) + x<sub>1</sub>(n)) mod 2

x<sub>2</sub>(n + 31) = (x<sub>2</sub>(n + 3) + x<sub>2</sub>(n + 2) + x<sub>2</sub>(n + 1) + x<sub>2</sub>(n)) mod 2

Where *N<sub>C</sub>* = 1600 and the first m-sequence *x<sub>1</sub>(n)* shall be initialized with *x<sub>1</sub>(0)* = 1, *x<sub>1</sub>(n)* = 0, n = 1, 2,... , 30.

The initialization of the second m-sequence *x<sub>2</sub>(n)*, is denoted by *c<sub>init</sub>* = \sum_{i=0}^{30} *x<sub>2</sub>(i)*.2<sup>i</sup> with the value depending on the application of the sequence.

### 5.3 OFDM baseband signal generation

### 5.4 Modulation and upconversion

## 6 Uplink

## 6.1 Overview

### 6.1.1 Physical channels

Uplink physical channel corresponds to a set of resource elements carrying higher layers infomation.

Defined uplink physical channels:
- Physical Uplink Shared Channel (PUSCH)
- Physical Uplink Control Channel (PUCCH)
- Physical Random Access Channel (PRACH)

### 6.1.2 Physical signals

Uplink physical signal is used by the physical layer but does not carry higher layers infomation.

Defined uplink physical signals:
- Demodulation reference signals (DM-RS)
- Phase-tracking reference signals (PT-RS)
- Sounding reference signal (SRS)

## 6.2 Physical resources

Defined antenna ports:
- Antenna ports starting with 0 for DM-RS for PUSCH
- Antenna ports starting with 1000 for SRS, PUSCH
- Antenna ports starting with 2000 for PUCCH
- Antenna ports 4000 for PRACH

## 6.3 Physical channels

### 6.3.1 PUSCH

#### 6.3.1.1 Scranbling

#### 6.3.1.2 Modulation

#### 6.3.1.3 Layer mapping

#### 6.3.1.4 Transform precoding

#### 6.3.1.5 Precoding

#### 6.3.1.5 Mapping to virtual resource blocks

#### 6.3.1.5 Mapping from virtual resource blocks

### 6.3.2 PUCCH

### 6.3.2.1 General

PUCCH supported formats:

|PUCCH<br>format|Length in OFDM symbols<br>N<sub>symb</sub>|Number<br>of bits|
|:-:|:-:|:-:|
|0|1-2|≤2|
|1|4-14|≤2|
|2|1-2|>2|
|3|4-14|>2|
|4|4-14|>2|

### 6.3.2.2 Sequence and cyclic shift hopping

PUCCH formats 0, 1, 3 and 4 use sequences *r<sup>(α, δ)</sup><sub>u, v</sub>* with *δ* = 0 where the sequence group *u* and the sequence number *v* depend on the [sequence hopping](#group-and-sequence-hopping) and the cyclic shift *α*.
depends on the [cyclic shift hopping](#cyclic-shift-hopping).

<h4 id="group-and-sequence-hopping"> 6.3.2.2.1 Group and sequence hopping</h4>

The sequence group *u* = (*f<sub>gh</sub>* + *f<sub>ss</sub>*) mod 30 and the sequence number *v* within the group depends on the higher-layer parameter *pucch-GroupHopping*:


<h4 id="cyclic-shift-hopping"> 6.3.2.2.2 Cyclic shift hopping</h4>













