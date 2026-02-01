**4 Functional Description**

- **Dynamic FIFO (DFIFO) sizing**, maximum to 1 KB

- Multiple modes of memory access
  - Scatter/Gather DMA mode
  - Buffer DMA mode
  - Slave mode

- Two integrated transceivers

**Device Mode Features**
- Endpoint 0 always present, bi-directional, consisting of EPO IN and EPO OUT
- Six additional endpoints 1–6, configurable as IN or OUT
- Maximum of five IN endpoints concurrently active at any time, including EPO IN
- All OUT endpoints share a single RX FIFO
- Each IN endpoint has a dedicated TX FIFO

**Host Mode Features**
- Eight host channels
- RX FIFO: shared by all periodic and non-periodic transactions
- Two TX FIFO:
  - One shared by all non-periodic transactions
  - One shared by all periodic transactions
- All of the above FIFOs share a 1 KB RAM.
- The size of each FIFO is configurable, with a maximum of 1 KB.

**Pin Assignment**
The pins connected to D+ and D- signals for two pairs of USB PHY are multiplexed with GPIO24–GPIO25 and GPIO26–GPIO27. The USB 2.0 Full-Speed OTG interface can use each of them. By default, the pins are multiplexed with GPIO26–GPIO27. In addition, the functionalities of USB _D-_ and USB _D+_ can be exchanged.
Other signals can be routed to any GPIOs via the GPIO matrix.

**4.2.2.11 USB Serial/JTAG Controller (USB_SERIAL_JTAG)**
ESP32-P4 contains a USB Serial/JTAG Controller. This unit can be used to program the SoC’s flash, read program output, as well as attach a debugger to the running program.

**Feature List**
- USB 2.0 full speed compliant, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- CDC-ACM virtual serial port and JTAG adapter functionality

Espressif Systems
69 ESP32-P4 Series Datasheet v0.6