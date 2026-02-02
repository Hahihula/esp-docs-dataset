**Title: Chapter 25 Two-Wire Automotive Interface (TWAI)**

---

### Figure Caption:
- **Figure 25.3-5. Layout of a Bit**

---

### Diagram Description:

The diagram shows the layout and structure of a bit in TWAI, with labels indicating different sections such as "SS", "PBS1", "PBS2". There is also an arrow labeled "Sample point".

---

### Figure Caption:
- **Figure 25.4-1. TWAI Overview Diagram**

---

**Subtitle: Registers Block (Section 25.4.1)**

The ESP32 CPU accesses peripherals as 32-bit aligned words. However, the majority of registers in the TWAI controller only contain useful data at least significant byte (bits [7:0]). Therefore, in these registers, bits [31:8] are ignored on writes and return O on reads.

#### Configuration Registers

The configuration registers store various configuration options for the TWAI controller such as bit rates, operating mode, Acceptance Filter etc. Configuration registers can only be modified whilst the TWAI controller is in Reset Mode (See Section 25.5.1).

#### Command Register

The command register is used by the CPU to drive the TWAI controller to initiate certain actions such as transmitting a message or clearing the Receive Buffer. The command register can also modify when the TWAI controller is Operation Mode.

---

**Footer:**
- Espresso Systems
- Page 535 (ESP32 TRM - Version 5.6)
- Submit Documentation Feedback