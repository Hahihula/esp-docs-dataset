

# 40.4 Architectural Overview

Figure 40.4-1 shows the architecture of MIPI CSI and its connection to other system components. The MIPI CSI consists of the following components:

*   **MIPI RX D-PHY:** Implements the physical link layer, including one clock lane (CP/CN) and two data lanes (DOP/DON and D1P/D1N) to connect with cameras.
*   **MIPI CSI-2 host:** Implements the CSI-2 protocol, receives camera data from D-PHY, and outputs through the Image Interface, which includes:

    *   Pipeline: Registers PPI signals.
    *   Descrambler: Converts PPI scrambled data to its original values when enabled.
    *   PHY adaptation layer: Manages the PHY interface, including PHY error handling.
    *   Packet analyzer: Processes received data from lanes, including data lane merging, header decoding, and various error detection and correction.
    *   Image interface: Reorders pixels into 32-bit Image Interface data and generates timing-accurate video synchronization signals.
    *   Error management: Monitors and notifies about error conditions on the CSI-2 link.
    *   Register bank: Provides access to configuration and control registers.

*   **PPI interface:** Connects the MIPI RX D-PHY and the MIPI CSI-2 host controller.
*   **Test code interface:** Sends configuration details from the MIPI CSI-2 host controller to the MIPI RX D-PHY.

Figure 40.4-1. MIPI CSI Architecture