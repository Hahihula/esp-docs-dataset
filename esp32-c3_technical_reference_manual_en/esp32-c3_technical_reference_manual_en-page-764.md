

```markdown
Chapter 30  
USB Serial/JTAG Controller (USB_SERIAL_JTAG)

## USB Serial/JTAG Controller (USB_SERIAL_JTAG)

The ESP32-C3 contains an USB Serial/JTAG Controller. This unit can be used to program the SoC’s flash, read program output, as well as attach a debugger to the running program. All of these are possible for any computer with a USB host ('host' in the rest of this text) without any active external components.

### 30.1 Overview

While programming and debugging an ESP32-C3 project using the UART and JTAG functionality is certainly possible, it has a few downsides. First of all, both UART and JTAG take up IO pins and as such, fewer pins are left usable for controlling external signals in software. Additionally, an external chip or adapter is needed for both UART and JTAG to interface with a host computer, which means it will be necessary to integrate these two functionalities in the form of external chips or debugging adapters.

In order to alleviate these issues,, as well as to negate the need for external devices, the ESP32-C3 contains an USB Serial/JTAG Controller, which integrates the functionality of both an USB-to-serial converter as well as those of an USB-to-JTAG adapter. As this device directly interfaces to an external USB host using only the two data lines required by USB2.0, debugging the ESP32-C3 only requires two pins to be dedicated to this functionality.

### 30.2 Features

*   USB Full-speed device.
*   Fixed function device, hardwired for CDC-ACM (Communication Device Class - Abstract Control Model) and JTAG adapter functionality.
*   2 OUT Endpoints, 3 IN Endpoints in addition to Control Endpoint 0; Up to 64-byte data payload size.
*   Internal PHY, so no or very few external components needed to connect to a host computer.
*   CDC-ACM adherent serial port emulation is plug-and-play on most modern OSes.
*   JTAG interface allows fast communication with CPU debug core using a compact representation of JTAG instructions.
*   CDC-ACM supports host controllable chip reset and entry into download mode.

As shown in Figure 30.2-1, the USB Serial/JTAG Controller consists of an USB PHY, a USB device interface, a JTAG command processor and a response capture unit, as well as the CDC-ACM registers. The PHY and part of the device interface are clocked from a 48 MHz clock derived from the main PLL, the rest of the logic is clocked from APB_CLK. The JTAG command processor is connected to the JTAG debug unit of the main processor; the CDC-ACM registers are connected to the APB bus and as such can be read from and written to by software running on the main CPU.
```