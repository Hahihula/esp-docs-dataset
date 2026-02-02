**Chapter Title:**
Chapter 25

**Section Heading:**
Two-Wire Automotive Interface (TWAI)

**Subsection and Content:**

#### Overview 
The Two-wire Automotive Interface (TWAI®) is a multi-master, multi-cast communication protocol with error detection and signaling and inbuilt message priorities and arbitration. The TWAI protocol is suited for automotive and industrial applications.

- **Note:** Please see [TWAI Protocol Description](#).

ESP32 contains a TWAI controller that can be connected to a TWAI bus via an external transceiver.
The TWAI controller contains numerous advanced features, and can be utilized in a wide range of use cases such as
automotive products, industrial automation controls, building automation etc.

#### Features 
ESP32 TWAI controller supports the following features:

- compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- Supports Standard Frame Format (11-bit ID) and Extended Frame Format (29-bit ID)

##### Bit rates:
- from 25 Kbit/s to 1 Mbit/s in chip revision v0.0/v1.0/v1.1
- from 12.5 Kbit/s to 1 Mbit/s in chip revision v3.0/v3.1

##### Multiple modes of operation
- Normal
- Listen Only (no influence on bus)
- Self Test (transmissions do not require acknowledgment)

##### Special transmissions:
- Single-shot transmissions (does not automatically re-transmit upon error)
- Self Reception (the TWAI controller transmits and receives messages simultaneously)

##### Acceptance Filter: 
(supports single and dual filter modes)

##### Error detection and handling
- Error counters
- Configurable Error Warning Limit

**Footer Information:**  
Espressif Systems  
525  
ESP32 TRM (Version 5.6)  

**Navigation Links:**  
[Submit Documentation Feedback](#)