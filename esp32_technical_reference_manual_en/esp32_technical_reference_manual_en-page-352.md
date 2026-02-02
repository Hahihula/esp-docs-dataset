**Chapter Title:**
Chapter 19 UART Controller (UART)

**Section and Register Descriptions with Details:**

- **Register 19.48, UHCI_DMA_OUT_DSCR_BFO_REG (0x5C)**
  - Description:
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```
  - Address of the last outlink descriptor `y-1`. (RO)

- **Register 19.49, UHCI_DMA_OUT_DSCR_BF1_REG (0x60)**
  - Description:
    ```
    0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    ```
  - Address of the second-to-last outlink descriptor `y-2`. (RO)

- **Register 19.50, UHCI_ESCAPE_CONF_REG (0x64)**
  - Description:
    ```
    8 7 6 5 4 3 2 1 0
    ```
  - Reserved bits.

**Flowchart:**
A flowchart is depicted showing the relationship between various escape control registers and their corresponding data paths, such as `UHCI_RX_13_ESC_EN`, `UHCI_TX_13_ESC_EN`, etc. The chart includes arrows indicating connections to different registers like `UHCI_RX_DB_ESC_EN` (R/W), `UHCI_TX_DB_ESC_EN` (R/W).

**Bit Definitions:**

- **UHCI_RX_13_ESC_EN**
  - Description:
    ```
    Set this bit to enable replacing flow control char 0x13, when DMA sends data.
    ```
  - Access type: R/W

- **UHCI_RX_11_ESC_EN**
  - Description:
    ```
    Set this bit to enable replacing flow control char 0x11, when DMA sends data.
    ```
  - Access type: R/W

- **UHCI_RX_DB_ESC_EN**
  - Description:
    ```
    Set this bit to enable replacing 0xdb char, when DMA sends data.
    ```
  - Access type: R/W

- **UHCI_RX_CO_ESC_EN**
  - Description:
    ```
    Set this bit to enable replacing 0xc0 char, when DMA sends data.
    ```
  - Access type: R/W

- **UHCI_TX_13_ESC_EN**
  - Description:
    ```
    Set this bit to enable decoding flow control char 0x13, when DMA receives data.
    ```
  - Access type: R/W

- **UHCI_TX_11_ESC_EN**
  - Description:
    ```
    Set this bit to enable decoding flow control char 0x11, when DMA receives data.
    ```
  - Access type: R/W

- **UHCI_TX_DB_ESC_EN**
  - Description:
    ```
    Set this bit to enable decoding 0xdb char, when DMA receives data.
    ```
  - Access type: R/W

- **UHCI_TX_CO_ESC_EN**
  - Description:
    ```
    Set this bit to enable decoding 0xc0 char, when DMA receives data.
    ```
  - Access type: R/W

**Footer Information:**
Espressif Systems
352 ESP32 TRM (Version 5.6)
Submit Documentation Feedback