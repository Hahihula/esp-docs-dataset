

```markdown
SSP_CFG[SSP_SRC] = SSP_SRC_NO_SSP

Sampling Point
Start of bit

SSP_CFG[SSP_OFFSET]

TRV_DELAY +

255

Figure 38.3-6. Secondary sampling point


Bit-rate Nominal Data
CAN frame BRS ESI DLC[3] DLC[2]
Sample point Start of bit SSP 1 SSP 2 SSP 3
BRS ESI Data Bit Time Length Data Bit Time Length
SSP Offset Time Length Time

Figure 38.3-7. Secondary sampling point 2


Secondary sampling point offset (TWAIFD_SSP_OFFSET) is configurable between 0 - 255. Internal range of secondary sampling point position is also 0 - 255. If due to some reason, the secondary sampling point position is more than 255 clock periods from start of bit (e.g. due to large measured transmitter delay), it will be saturated to 255.

Since CAN FD input delay is 2 system clock periods (minimum time quanta), position of secondary sampling point should be configured to at least 2 to compensate its own input delay. If TWAIFD_SSP_OFFSET < 3 and TWAIFD_SSP_SRC = SSP_SRC_OFFSET, it is impossible to transmitt CAN FD frames without detecting bit errors on CAN FD's own transmitted frames.

CAN FD can handle at most 4 bits on flight between CAN_TX and CAN_RX pins when using the secondary sampling point. For instance, if system clock = 100 MHz and data bit rate = 5 Mbit/s, then one data bit time = 20 system clock periods. Then, the latest possible position of secondary sampling point is 20 × 4 = 80 system clock periods. This limitation applies to the final position of secondary sampling point (with TWAIFD_SSP_OFFSET/TWAIFD_TRV_DELAY_VALUE included). Users should not configure the secondary sample point position later than 4 data bit times.

38.3.7.4 CAN FD Support

CAN FD supports both ISO and non-ISO versions of CAN FD protocols. Selection between these two versions is done via TWAIFD_NISOFD register. When the ISO protocol version is chosen, CAN FD is conformant to ISO11898-1:2015. When the non-ISO version is chosen, CAN FD conforms to CAN FD specification 1.0. TWAIFD_NISOFD can be modified only when CAN FD is disabled (TWAIFD_ENA = 0).
```