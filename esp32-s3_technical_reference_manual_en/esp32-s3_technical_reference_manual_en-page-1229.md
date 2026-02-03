**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Body Text:**

time-division multiplexing one USB controller connects to internal transceiver and the other one connects to an external transceiver.

When only internal transceiver is used, it is shared by USB OTG and USB Serial/JTAG. In default, internal transceiver is connected to USB Serial/JTAG. When RTC_CNTL_SW _HW_USB_PHY_SEL_CFG is 0, the connection of internal transceiver is controlled by efuse bit EFUSE_USB_PHY_SEL. When EFUSE_USB_PHY_SEL is 0, internal transceiver is connected with USB Serial/JTAG. Otherwise, it is connected to USB OTG. When RTC_CNTL_SW _HW_USB_PHY SEL_CFG is 1, the connection switching is controlled by RTC_CNTL_SW _USB_PHY_SEL_CFG(it has the same meaning with EFUSE_USB_PHY_SEL).

When both internal transceiver and external transceiver are used, one USB controller select one of transceivers, the other would select the other transceiver. The specific connection mapping please refer to Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG).

- **Subsection Title:**
  - USB External Controller

The USB External Controller is primarily used to control the routing of the USB 2.0 FS serial interface to either the internal or external transceiver. The External Controller can also enable a power saving mode by gating the controller core's clock (AHB clock) or powering down the connected SPRAM. Note that this power saving mode is different for the power savings via SRP.

- **Subsection Title:**
  - Data FIFO RAM Interface

The multiple FIFOs used by the controller core are not actually located within the controller core itself, but on the SPRAM (Single-Port RAM). FIFOs are dynamically sized, thus are allocated at run-time in the SPRAM. When the CPU, DMA, or the controller core attempts to read/write to FIFOs, those accesses are routed through the data FIFO RAM interface.

**Subsection Title:**
32.3.2 Memory Layout

The following diagram illustrates the memory layout of the OTG_FS registers which are used to configure and control the USB Controller Core. Note that USB External Controller uses a separate set of registers (called wrap registers).

**Subsection Title:**
32.3.2.1 Control & Status Registers

- **Sub-subsection Title: Global CSRs**

These registers are responsible for the configuration/control/status of the global features of OTG_FS (i.e., features which are common to both Host and Device modes). These features include OTG control (HNP, SRP, and A/B-device detection), USB configuration (selecting Host or Device mode and PHY selection), and system-level interrupts. Software can access these registers whilst in Host or Device modes.

- **Sub-subsection Title: Host Mode CSRs**

These registers are responsible for the configuration/control/status when operating in Host mode, thus should only be accessed when operating in Host mode. Each channel will have its own set of registers within the Host mode CSRs.

- **Sub-subsection Title: Device Mode CSRs**

These registers are responsible for the configuration/control/status when operating in Device mode, thus should only be accessed when operating in Device mode. Each Endpoint will have its own set of registers within the Device mode CSRs.

**Footer Information:**
Espressif Systems
1229 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback