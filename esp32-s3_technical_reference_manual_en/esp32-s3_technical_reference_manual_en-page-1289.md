**Title: Chapter 34 SD/MMC Host Controller (SDHOST)**

---

### Register Section:
- **Register Name:** SDHOST_INTMASK_REG (0x0024)

#### Diagram Description:
The diagram shows a register layout with specific bits labeled for different functions. The labels include:

- `31` to `0`: These are the bit positions in hexadecimal format.
- `SDHOST_SDIO_INT_MASK`: This is described as an SDIO interrupt mask, one bit per card.

#### Text Explanation of Bits:
- **SDHOST_SDIO_INT_MASK:** 
  - Description: "SDIO interrupt mask. One bit for each card."
  - Bit Positions (15 to 0): Corresponding bits in the register.
  - Functionality when masked or unmasked, and what it enables.

#### Detailed List of Bits:
- **Bit 15 (EBE):** End-bit error/no CRC error
- **Bit 14 (ACD):** Auto command done
- **Bit 13 (SBE/BCI):** Rx Start Bit Error
- **Bit 12 (HLE):** Hardware locked write error
- **Bit 11 (FRUN):** FIFO underrun/overrun error
- **Bit 10 (HTO):** Data starvation-by-host timeout
- **Bit 9 (DRTO):** Data read timeout
- **Bit 8 (RTO):** Response timeout
- **Bit 7 (DCRC):** Data CRC error
- **Bit 6 (RCRC):** Response CRC error
- **Bit 5 (RXDR):** Receive FIFO data request
- **Bit 4 (TXDR):** Transmit FIFO data request
- **Bit 3 (DTO):** Data transfer over
- **Bit 2 (CD):** Command done
- **Bit 1 (RE):** Response error
- **Bit 0 (CD):** Card detect

---

### Another Register Section:
- **Register Name:** SDHOST_CMDARG_REG (0x0028)

#### Text Explanation of the Register:
- "Value indicates command argument to be passed to the card. (R/W)"

---

**Footer:**
- Page number and document version information.
  - Espressif Systems
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback

--- 

This is a structured description of all text content from the image, including headings, lists, diagrams with labels, etc., formatted in Markdown as requested without conversational context or additional interpretation beyond what's visible and described directly within the document itself.