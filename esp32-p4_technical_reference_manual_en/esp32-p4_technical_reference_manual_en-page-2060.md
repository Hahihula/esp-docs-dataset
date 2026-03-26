

```markdown
Data lane    The data lane of the MIPI D-PHY interface, used to transmit data and commands.
Line         The line of the data lane of the MIPI D-PHY interface; each data lane consists of two lines: P and N.
Sequence     A string of state codes received through the data lane, controlling the MIPI RX D-PHY to enter other modes from Control mode.
Control mode One of the operating modes of the MIPI RX D-PHY, used to receive requests from the transmitter. All other modes return to this mode.
High-Speed Data Reception mode    One of the operating modes of the MIPI RX D-PHY, used to receive data in burst mode.
Escape mode   One of the operating modes of the MIPI RX D-PHY, used to support low-speed asynchronous communication on the data lane to maintain a low-power state.
Ultra Low Power State (ULPS)      One of the operating modes of the MIPI RX D-PHY, in which the clock lane and data lane are in idle state, maintaining the lowest power consumption except for the Shut-Down state.
Test code     Specific control or configuration codes used to manage and test the MIPI D-PHY, such as setting operational mode.
```

## 40.3 Feature List

MIPI CSI in ESP32-P4 supports the following features:

*   MIPI RX D-PHY compliant with MIPI D-PHY interface specification revision 1.1
*   MIPI CSI-2 host compliant with MIPI CSI-2 specification
*   Two data lanes, each with a rate ranging from 80 Mbps to 1.5 Gbps
*   Ultra Low Power State in Escape mode
*   32-bit image interface with ISP
*   Various input image formats:
    *   RGB888/RGB666/RGB565
    *   YUV422/YUV420
    *   RAW8/RAW10/RAW12
*   Error detection and correction at PHY level, packet level, line level, and frame level
*   Electromagnetic Interference (EMI) mitigation by data scrambling

**Note:**
ESP32-P4 does not support different virtual channels defined in the MIPI specification, so virtual channel numbers in the packet header are ignored.
```