**Title:**
Table 30.5-4. SPI3 bus Signals Used in Various SPI Modes

**Columns Headers (from left to right):**
1. Master Mode - FD, Dual SPI HD, Quad SPI QPI
2. Slave Mode - FD, Dual SPI HD, Quad SPI QPI

**Rows:**

- **SPI3_CLK**: 
  - Master Mode:
    - FD: Y
    - Dual SPI HD: Y
    - Quad SPI QPI: Y
  - Slave Mode (all): Y

- **SPI3_CS0**: 
  - Master Mode:
    - FD: Y
    - Dual SPI HD: Y
    - Quad SPI QPI: Y
  - Slave Mode (all): Y

- **SPI3_CS1**: 
  - Master Mode:
    - FD: Y
    - Dual SPI HD: Y
    - Quad SPI QPI: Y
  - Slave Mode (all): Y

- **SPI3_CS2**: 
  - Master Mode:
    - FD: Y
    - Dual SPI HD: Y
    - Quad SPI QPI: Y
  - Slave Mode (all): Y

- **SPI3_D**: 
  - Master Mode:
    - FD: Y
    - Dual SPI HD: v4
    - Quad SPI QPI: Y
  - Slave Mode:
    - FD: Y
    - Dual SPI HD: v6
    - Quad SPI QPI: Y

- **SPI3_Q**: 
  - Master Mode (all): Y
  - Slave Mode (all): Y

- **SPI3_WP**: 
  - Master Mode:
    - FD: Y
    - Dual SPI HD: Y
    - Quad SPI QPI: v5
  - Slave Mode (all): Y

- **SPI3_HD**: 
  - Master Mode:
    - FD: Y
    - Dual SPI HD: Y
    - Quad SPI QPI: Y
  - Slave Mode (all): Y

**Footnotes and Definitions at the bottom of table:**
1. FD: full-duplex.
2. HD: half-duplex.

3-8. Descriptions for each signal:
   - Only one of the two signals is used at a time.
   - The four signals are in parallel (repeated three times).
   - 7 and 8 refer to "The feedbacks" which means that only when there's an active change on these lines, they will be updated.

**Side Text:**
- ESP32-S3 TRM (Version 1.0)

**Additional Information at the bottom left corner of page image:** 
- Submit Documentation Feedback

**Additional Page Number and Navigation:**
- GoBack
- Chapter Title is partially visible as "Chapter 30 SPI Controller"