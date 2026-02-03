**Title: Chapter 3 GDMA Controller (GDMA)**

**Subtitle: Register 3.16. GDMA_OUT_INT_ST_CHn_REG**

- **Description:** 
  - `GDMA_OUTDone_CHn_INT_ST`: The raw interrupt status bit for the GDMA_OUT_DONE_CH_INT interrupt.
  - `GDMA_OUT_EOF_CHn_INT_ST`: The raw interrupt status bit for the GDMA_OUT_EOF_CH_INT interrupt.
  - `GDMA_OUT_DSCR_ERR_CHn_INT_ST`: The raw interrupt status bit for the GDMA_OUT_DSCR_ERR_CH_INT interrupt.

**Subtitle: Register 3.17. GDMA_OUT_INT_ENA_CHn_REG**

- **Description:** 
  - `GDMA_OUT_DONE_CHn_INT_ENA`: The interrupt enable bit for the GDMA_OUT_DONE_CH_INT interrupt.
  - `GDMA_OUT_EOF_CHn_INT_ENA`: The interrupt enable bit for the GDMA_OUT_EOF_CH_INT interrupt.
  - `GDMA_OUT_DSCR_ERR_CHn_INT_ENA`: The interrupt enable bit for the GDMA_OUT_DSCR_ERR_CH_INT interrupt.

**Footer:**
- "Espressif Systems"
- Page number and document version information:
  - "387 ESP32-S3 TRM (Version 1.7)"
- Link to submit documentation feedback

**Diagram Description:** 
The diagram shows a bit map for the registers, with each register having specific bits labeled as follows:

- `GDMA_OUT_TOTAL_EOF_CHO_INT_ENA`: Reset
- `GDMA_OUTTotal_DSCR_ERR_CHO_INT_ENA`: Reset
- `GDMA_OUTDone_CHO_INT_ENA`: Reset

Each of these labels corresponds to a bit in the diagram, indicating their position and function within each register. The bits are numbered from 31 (most significant) down to 0.

**Note:** There is an indication that some parts have been reserved or not specified ("reserved").