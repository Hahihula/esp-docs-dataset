**Title:**
Chapter 30 Remote Control Peripheral (RMT)

**Diagram Labels and Descriptions:**

- **Figure 30.2-1. RMT Architecture:** This diagram illustrates the architecture of a Remote Memory Transfer peripheral, showing various components such as RAM blocks (`block0`, `block1`, etc.), clock division units, divider bits, carrier generator, modulator, comparator, counter, receiver filter, and more.

**Figure 30.2-2. Data Structure:**

- **Table Description:** The table shows the data structure for RMT channels with columns labeled as follows:
  - `addr`: Address
  - `level`: Level (15 bits)
  - `period`: Period

**Text Explanation of Figure 30.2-2:**
The RAM address range is defined by a formula involving variables such as `start_addr_CHn`, `end_addr_CHn`, and the number of channels (`n`). The addresses are calculated using modulo operations.

**Additional Information in Text Below Diagrams:**

To protect against overwriting, blocks can be designated to own specific roles (transmitter or receiver) within a channel's RAM block. If this designation is violated, an RMT_CHn_ERR interrupt will occur.
- **Note:** When enabling continuous transmission mode by setting `RMT_REG_TX_CONTI_MODE`, the transmitter continuously transmits data from one byte sequence through another without interruption.

**Footer:**
Espressif Systems
728 ESP32 TRM (Version 5.6)
Submit Documentation Feedback