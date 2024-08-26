# GPON
## Background information
GPON is an alternative to Etrhernet switching in campus networking. Replaces the traditional three-tier Ethernet design with a two-tier optic network which eleminates access and distribution Ethernet switches with passive optical devices.
## Terminology
- Gigabit-capable Passive Optical Network **(GPON)** - Standard for **passive optical networks (PON)** published by the **ITU-T**.
- Optical Distribution Network **(ODN)** - The **physical fibre and optical devices** that distribute signal to users in telecommunications network. The **ODN** is composed of **passive optical components** (POS), such as optical fibers, and one or more passive optical splitters.
- Optical Network Ternimation **(ONT)**/ Optical Network Units **(ONU)** - **Connects** end-user **devices** into **the GPON network**. **Provides** the **optical to electrical signal conversion**. ONTs provide **AES encryption** via ONT key.
- Splitters - Used to aggregate or multiplex fiber optic signas to a single upstream fiber optical cable. (1:32 ratio)
- Optical Line Terminal **(OLT)** - Device that **aggregates** all **optical signals from ONTs** into a **single multiplexed beam of light** which is then **converted into an electrical signal**, formatted to Ethernet packet type standards for Layer 2 or Layer 3 forwarding.
- Wavelength-Division Multiplexing **(WDM)** - Wavelength-division multiplexing is a technology that multiplexes a number of optical carrier signals onto a single optical fiber that uses different wavelengths of laser light.
- GEM GPON encapsulation method (GEM) - A data frame transport scheme used in gigabit capable passive optical network

## Network diagram
![Annotation 2024-08-25 235908](https://github.com/user-attachments/assets/6133fd3c-fc2b-4fc2-bc8b-8fa9df51670c)

## Technology overview
![Annotation 2024-08-26 001719](https://github.com/user-attachments/assets/c6c669c7-9e75-4dab-99c3-12143d22c3d9)
- The **OLT** is connected to the **optical splitter** through a single optical fiber, and then the optical splitter connects to ONUs/ONTs.
- **GPON** adopts **WDM** to transmit data of different upstream/downstream wavelengths over the same ODN. Wavelengths range from 1290 - 1300 nm in the upstream direction and from 1480 - 1500 nm in the downstream direction.
- Data is broadcast in the downstream direction, and in the upstream direction data is burst in time-division multiple access (TDMA) mode (based on timeslots).
- Support point-to-mulitpoint (P2MP) multicast transmission.

## GPON limits
- Maximum logical reach: 60km (This is the maximum distance managed by the higher layers of the system (MAC, TC, Ranging), in view of a (= according to) future physical media dependent (PMD) specification (thong so ky thuat)).
- Maximum fiber distance between send/receiver (S/R) and receive/send (R/S) points: **20km**
- Maximum differential fiber distance: **20km**
- Split ratio: Restricted by path loss, PON with passive splitters **(16, 32, or 64 way split)**
- Rate: 1.24416 Gigabits/s up, 2.48832 Gigabits/s down

## Advanced Encryption Strandard AES Encryption
- The OLT initiates the process - requests a key from the ONU
- The ONU generates the key and sends it to the OLT
- The OLT defines the key Switching Time and the encrypted ports and notifies the ONU


