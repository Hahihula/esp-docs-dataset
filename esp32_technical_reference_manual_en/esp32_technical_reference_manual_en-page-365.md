**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Table Headers:**
- Name
- Description
- SPI0
- SPI1
- SPI2
- SPI3
- Acc

**Table Rows and Content:**

1. **Name:** SPI_OUT_EOF_BFR_DESC_ADDR_REG  
   **Description:** Relative buffer address where EOF occurs  
   **SPI0:** 3FF43134  
   **SPI1:** 3FF42134  
   **SPI2:** 3FF64134  
   **SPI3:** 3FF65134  
   **Acc:** RO

2. **Name:** SPI_OUT_EOF_DESC_ADDR_REG  
   **Description:** Descriptor address where EOF occurs  
   **SPI0:** 3FF43138  
   **SPI1:** 3FF42138  
   **SPI2:** 3FF64138  
   **SPI3:** 3FF65138  
   **Acc:** RO

3. **Name:** SPI_OUTLINK_DSCR_REG  
   **Description:** Current descriptor pointer  
   **SPI0:** 3FF4313C  
   **SPI1:** 3FF4213C  
   **SPI2:** 3FF6413C  
   **SPI3:** 3FF6513C  
   **Acc:** RO

4. **Name:** SPI_OUTLINK_DSCR_BFO_REG  
   **Description:** Next descriptor data pointer  
   **SPI0:** 3FF43140  
   **SPI1:** 3FF42140  
   **SPI2:** 3FF64140  
   **SPI3:** 3FF65140  
   **Acc:** RO

5. **Name:** SPI_OUTLINK_DSCR_BF1_REG  
   **Description:** Current descriptor data pointer  
   **SPI0:** 3FF43144  
   **SPI1:** 3FF42144  
   **SPI2:** 3FF64144  
   **SPI3:** 3FF65144  
   **Acc:** RO

6. **Name:** SPI_DMA_RSTATUS_REG  
   **Description:** DMA memory read status  
   **SPI0:** 3FF43148  
   **SPI1:** 3FF42148  
   **SPI2:** 3FF64148  
   **SPI3:** 3FF65148  
   **Acc:** RO

7. **Name:** SPI_DMA_TSTATUS_REG  
   **Description:** DMA memory write status  
   **SPI0:** 3FF4314C  
   **SPI1:** 3FF4214C  
   **SPI2:** 3FF6414C  
   **SPI3:** 3FF6514C  
   **Acc:** RO

**Subsection Title:**
DMA interrupt registers

8. **Name:** SPI_DMA_INT_RAW_REG  
   **Description:** Raw interrupt status  
   **SPI0:** 3FF43114  
   **SPI1:** 3FF42114  
   **SPI2:** 3FF64114  
   **SPI3:** 3FF65114  
   **Acc:** RO

9. **Name:** SPI_DMA_INT_ST_REG  
   **Description:** Masked interrupt status  
   **SPI0:** 3FF43118  
   **SPI1:** 3FF42118  
   **SPI2:** 3FF64118  
   **SPI3:** 3FF65118  
   **Acc:** RO

10. **Name:** SPI_DMA_INT_ENA_REG  
    **Description:** Interrupt enable bits  
    **SPI0:** 3FF43110  
    **SPI1:** 3FF42110  
    **SPI2:** 3FF64110  
    **SPI3:** 3FF65110  
    **Acc:** R/W

11. **Name:** SPI_DMA_INT_CLR_REG  
    **Description:** Interrupt clear bits  
    **SPI0:** 3FF4311C  
    **SPI1:** 3FF4211C  
    **SPI2:** 3FF6411C  
    **SPI3:** 3FF6511C  
    **Acc:** R/W

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback