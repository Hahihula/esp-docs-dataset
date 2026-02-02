**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Back Button:**
GoBack

**Register Information Table Header:**
- Register Name | Offset in Word/Byte | Description
- CEATA_DEVICE_INTERRUPT_STATUS | 0x0000 | Various bits with descriptions.

**Table Details for CEATA_DEVICE_INTERRUPT_STATUS:**
- Bits are labeled from right to left as follows:
  - (reserved)
  - SEND_AUTO_STOP_CCSD
  - SEND_CCSD
  - SEND'READ_DATA
  - SEND'READ_WAIT
  - SEND'READ_RESPONSE
  - SEND'READ尼亚
  - SEND'READ尼亚
  - SEND'READ尼亚
  - SEND'READ尼亚
  - (reserved)
  - DMA_RESET
  - FIFO_RESET
  - CONTROLLER_RESET

**Text Sections:**

1. **CEATA_DEVICE_INTERRUPT_STATUS Description:**
   Software should appropriately write to this bit after the power-on reset or any other reset to the CE-ATA device.
   After reset, the CE-ATA device's interrupt is usually disabled (nIEN = 1).
   If the host enables the CE-ATA device’s interrupt,
   then software should set this bit. (R/W)

2. **SEND_AUTO_STOP_CCSD:**
   Always set send_auto_stop_ccsd and send_ccsd bits together;
   send_auto_stop_ccsd should not be set independently of send_ccsd.
   When set, SD/MMC automatically sends an internally-generated STOP command (CMD12) to the CE-ATA device. After sending this
   internally-generated STOP command,
   the Auto Command Done (ACD) bit in RINTSTS is set and an interrupt is generated for the host; 
   if ACD interrupt not masked.
   After sending the Command Completion Signal Disable (CCSD), SD/MMC automatically clears send_auto_stop_ccsd bits. 

3. **SEND_CCSD:**
   When set, SD/MMC sends CCSD to CE-ATA device,
   Software sets this bit only
   current command is expecting CCS (that is RW_BLK),
   and if interrupts are enabled for the 
   CE-ATA device.
   Once ACD pattern sent to it, SD/MMC automatically clears send_ccsd bit. It also sets Command Done in RINTSTS register;
   generates an interrupt for host; case
   Command Done interrupt not masked.

4. **ABORT_READ_DATA:**
   After suspend-command is issued during read operation,
   software polls the card find when 
   suspend-event occurred.
   Once this event has happened, Software sets bit which will reset data state machine waiting next block of data;
   This bit automatically cleared once
   Data State Machine

5. **SEND_IRQ_RESPONSE:**
   Bit clears once response is sent; to wait for MMC card interrupts,
   host issues CMD40 and waits for interrupt from MMC cards.
   If the host wants SD/MMC exit waiting for interrupt state, it can set this bit;
   at which time
   SD/MMC command state-machine sends CMD40 on bus

**Footer:**
Continued on next page...

**Document Footer Information:**
Espressif Systems | 611 ESP32 TRM (Version 5.6) Submit Documentation Feedback