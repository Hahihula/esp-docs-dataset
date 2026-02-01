Title: Functional Description

Body Text:
The clock generator has built-in calibration and self-test circuits. Quadrature clock phases and phase noise are optimized on chip with patented calibration algorithms which ensure the best performance of the receiver and the transmitter.

Subtitle 1: 4.3.2 Wi-Fi

Body Text under Subtitle 1:
This subsection describes the chip’s Wi-Fi capabilities, which facilitate wireless communication at a high data rate.

Subtitle 2: 4.3.2.1 Wi-Fi Radio and Baseband

List items (indented):
- The ESP32-C6 Wi-Fi radio and baseband support the following features:

    - compliant with IEEE 802.11b/g/n/ax
    - 1T1R in 2.4 GHz band
    - 802.11ax

    - 20 MHz-only non-AP mode
    - MCS0 ~ MCS9
    - Uplink and downlink OFDMA
    - Downlink MU-MIMO (multi-user, multiple input, multiple output)
    - Longer OFDM symbol, with 0.8, 1.6, 3.2 µs guard interval
    - DCM (dual carrier modulation), up to 16-QAM
    - Single-user/multi-user beamformee
    - Channel quality indication (CQI)
    - RX STBC (single spatial stream)

- 802.11b/g/n

    - MCS0 ~ MCS7 that supports 20 MHz and 40 MHz bandwidth
    - MCS32
        - Data rate up to 150 Mbps
        - 0.4 µs guard interval

    - adjustable transmitting power

- antenna diversity

ESP32-C6 supports antenna diversity with an external RF switch. This switch is controlled by one or more GPIOs, and used to select the best antenna to minimize the effects of channel imperfections.

Subtitle 3: 4.3.2.2 Wi-Fi MAC

Body Text under Subtitle 3:
ESP32-C6 implements the full IEEE 802.11 b/g/n/ax Wi-Fi MAC protocol. It supports the Basic Service Set (BSS) STA and SoftAP operations under the Distributed Control Function (DCF). Power management is handled automatically with minimal host interaction to minimize the active duty period.

Footer:
Espressif Systems
60

Link Text: Submit Documentation Feedback

Document Reference at Bottom Right Corner:
ESP32-C6 Series Datasheet v1.4