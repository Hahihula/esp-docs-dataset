**Title:**
1. Schematic Design

**Figure Caption and Diagram Description:**
- **Figure 1-7. Reference Circuit for USB-UART Chip**

**Body Text with Subsections:**

### 1.3.5 Strapping Pins and Other Special Pins

- GPIO0 is one of the strapping pins, and its level state in the power-on reset process is related to download:
  - “1”: enter Flash startup mode, and the chip defaults to “1”.
  - “0”: enter download mode.

- Meanwhile, GPIO0 can also connect to other chips, such as MCLK (master clock), so using GPIO0 for other functions is not recommended.

- GPIO2 is another strapping pin, and its level state in the power-on reset process is also related to download:
  - “0”: enter download mode, and the chip defaults to “0”.

- Meanwhile, GPIO2 can be used for connection to SDIO/MMC (for example, SD card), so using GPIO2 for other purposes is not recommended.

**Note:**
In your design, it is recommended to reserve test points for GPIO0 and GPIO2, or to connect a button for downloading.
For example:

**Footer Information:**
- Page number: 6/19
- Date of publication: January 2019 (2019.01)