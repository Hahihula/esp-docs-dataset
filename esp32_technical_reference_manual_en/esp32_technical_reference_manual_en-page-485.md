**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Subtitles and Lists with Descriptions, Addresses, and Access Types**

1. **Read, Self Set, and Read Clear (R/SS/RC)**
   - Latched-low (LL)
   - Latched-high (LH)

2. **DMA configuration and control registers:**
   - DMABUSMODE_REG
     - Description: Bus mode configuration
     - Address: 0x3FF69000
     - Access: R/WS/SC

   - DMATXPOLLDemand_REG
     - Description: Pull demand for data transmit
     - Address: 0x3FF69004
     - Access: RO/WT

   - DMRXPollDemand_REG
     - Description: Pull demand for data receive
     - Address: 0x3FF69008
     - Access: R/O/WT

   - DMARXBASEADDR_REG
     - Description: Base address of the first receive descriptor
     - Address: 0x3FF6900C
     - Access: R/W

   - DMATXBASEADDR_REG
     - Description: Base address of the first transmit descriptor
     - Address: 0x3FF69010
     - Access: R/W

   - DMASTATUS_REG
     - Description: State of interrupts, errors and other events
     - Address: 0x3FF69014
     - Access: R/SS/WC

   - DMAOPERATION_MODE_REG
     - Description: Receive and Transmit operating modes and command
     - Address: 0x3FF69018
     - Access: R/SS/WC

   - DMAIN_EN_REG
     - Description: Enable / disable interrupts
     - Address: 0x3FF6901C
     - Access: R/W

   - DMAMISSEDFR_REG
     - Description: Missed Frame and Buffer Overflow Counter Register
     - Address: 0x3FF69020
     - Access: R/W

   - DMRINTWDTIMER_REG
     - Description: Watchdog timer count on receive
     - Address: 0x3FF69024
     - Access: R/W

   - DMATXCURRDSC_REG
     - Description: Pointer to current transmit descriptor
     - Address: 0x3FF69048
     - Access: RO

   - DMARXCURRDESC_REG
     - Description: Pointer to current receive descriptor
     - Address: 0x3FF6904C
     - Access: R/O

   - DMATXCURRADDR_BUF_REG
     - Description: Pointer to current transmit buffer
     - Address: 0x3FF69050
     - Access: RO

   - DMRXCURRADDR_BUF_REG
     - Description: Pointer to current receive buffer
     - Address: 0x3FF69054
     - Access: R/O

3. **MAC configuration and control registers:**
   - EMACCONFIG_REG
     - Description: MAC configuration
     - Address: 0x3FF6A000
     - Access: R/W

   - EMACFF_REG
     - Description: Frame filter settings
     - Address: 0x3FF6A004
     - Access: R/W

   - EMACGMIIDADDR_REG
     - Description: PHY configuration access
     - Address: 0x3FF6A010
     - Access: R/WS/SC

   - EMACMIIDATA_REG
     - Description: PHY data read write
     - Address: 0x3FF6A014
     - Access: R/W

   - EMACFCReg
     - Description: frame flow control
     - Address: 0x3FF6A018
     - Access: R/WS/SC(FCB)

   - EMACDEBUG_REG
     - Description: Status debugging bits
     - Address: 0x3FF6A024
     - Access: RO

   - PMT_RWUFR_REG
     - Description: Remote Wake-Up Frame Filter
     - Address: 0x3FF6A028
     - Access: R/O

   - PMT_CSR_REG
     - Description: PMT Control and Status
     - Address: 0x3FF6A02C
     - Access: RO

   - EMACLPI_CSR_REG
     - Description: LPI Control and Status
     - Address: 0x3FF6A030
     - Access: R/O

   - EMACLPITIMERSCONTROL_REG
     - Description: LPI Timers Control
     - Address: 0x3FF6A034
     - Access: RO

   - EMACINTSReg
     - Description: Interrupt status
     - Address: 0x3FF6A038
     - Access: R/O

   - EMACINTMASK_REG
     - Description: Interrupt mask
     - Address: 0x3FF6A03C
     - Access: R/W

   - EMACADDROHIGH_REG
     - Description: Upper 16 bits of the first 6-byte MAC address
     - Address: 0x3FF6A040
     - Access: R/W

   - EMACADDROLOW_REG
     - Description: Lower 32 bits of the first 6-byte MAC address
     - Address: 0x3FF6A044
     - Access: R/W

**Footer Information**
- Page Number: 485
- Document Version: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems
- Link Texts:
  - Submit Documentation Feedback