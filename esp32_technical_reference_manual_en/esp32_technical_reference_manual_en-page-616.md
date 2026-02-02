**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Titles and Content:**

1. **Register 27.0. CMDARG_REG (0x0028)**
   - **CMDARG_REG**: Value indicates command argument to be passed to the card. (R/W)
   
2. **Register 27.11. CMD_REG (0x002C)**

3. **Bit Description Table:**
   ```
   START_CMD
     0 1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
   ```
   - **START_CMD**: Start command. Once command is served by the CIU, this bit is automatically cleared.
     When this bit is set, host should not attempt to write to any command registers. If a write is attempted, hardware lock error is set in raw interrupt register. Once command is sent and a response is received from SD_MMC_CEATA cards, Command Done bit is set in the raw interrupt Register.

4. **USE_HOLE**
   - Use Hold Register.
     (R/W): CMD and DATA sent to card bypassing HOLD Register; 1: CMD and DATA sent to card through the HOLD Register

5. **CCSEXPECTED**
   - Expected Command Completion Signal (CCS) configuration
     O: Interrupts are not enabled in CE-ATA device (nIEN = 1 in ATA control register), or command does not expect CCS from device.
       1: Interrupts are enabled in CE-ATA device (nIEN = 0), and RW_BLK command expects command completion signal from CE-ATA device.

6. **READ_CEATA_DEVICE**
   - Read access flag
     O: Host is not performing read access towards CE-ATA device; 
       1: Host is performing read access to CE-ATA device.
     Software should set this bit to indicate that CE-ATA device being accessed for read transfer.
     This bit used to disable read data timeout indication while performing CE-ATA read transfers. Maximum value of I/O transmission delay can be no less than 10 seconds.

**Footer:**
Continued on the next page...

**Company Information and Document Details:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:** 
616