**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Continued from the previous page**

**Register Section - Register 34.1, SDHOST_CTRL_REG (0x0000):**

- **SDHOST_ABORT_READ_DATA**: After a suspend-command is issued during a read-operation, software polls the card to find when the suspend-event occurred. Once the suspend-event has occurred, software sets the bit which will reset the data state machine that is waiting for the next block of data. This bit is automatically cleared once the data state machine is reset to idle.
  - **Type:** (R/W)

- **SDHOST_SEND_IRQ_RESPONSE**: Bit automatically clears once response is sent. To wait for MMC card interrupts, host issues CMD40 and waits for interrupt response from MMC card(s). In the meantime, if host wants SD/MMC to exit waiting for interrupt state, it can set this bit, at which time SD/MMC command-state-machine sends CMD40 response on bus and returns to idle state.
  - **Type:** (R/W)

- **SDHOST_READ_WAIT**: For sending read-wait to SDIO cards. This is a wait operation that allows the host controller to pause during data transfer until it receives an interrupt or other signal indicating completion of the transaction with the card(s).
  - **Type:** (R/W)

- **SDHOST_INT_ENABLE**: Global interrupt enable/disable bit.
  - `0: Disable`
  - `1: Enable`
  - This is a read/write register.

- **SDHOST_DMA_RESET**: To reset DMA interface, firmware should set this bit to 1. This bit is auto-cleared after two AHB clocks.
  - **Type:** (R/W)

- **SDHOST_FIFO_RESET**: To reset FIFO, firmware should set the bit to 1. This bit is auto-cleared after completion of reset operation in addition to synchronization delay and clock cycles required for system recovery from a reset state or error condition that caused the need for a reset.
  - Note: FIFO pointers will be out of reset after two cycles of system clocks, plus an additional cycle (2 cycles) before the FIFO_reset is cleared.

- **SDHOST_CONTROLLER_RESET**: To reset controller, firmware should set this bit. This bit is auto-cleared after AHB and two sdhost_clk_in clock cycles.
  - **Type:** (R/W)

**Register Section - Register 34.2, SDHOST_CLKDIV_REG (0x0008):**

- The register contains multiple fields for controlling the clock division:
  - `SDHOST_CLK_DIVIDER[31:0]`: Clock divider value.
    - **Description:** Clock divisor is \(2^n\), where \(n = 0\) bypasses the divider, and a value of 1 means divided by 2. For example, if n=5 then it divides clock frequency into \(\frac{1}{32}\)th part.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback