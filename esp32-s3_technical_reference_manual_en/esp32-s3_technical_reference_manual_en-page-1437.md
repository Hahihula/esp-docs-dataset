**Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Diagram Description:**
The diagram shows a register map for RMT_INT_CLR_REG, with various interrupt clear registers labeled from "RMT_CHn_TX_END_INTC" to "RMT_CHn_RXTHR_EVENT_INTC". Each label is associated with an interrupt number and some are marked as "(reserved)".

**Text Content (List of Interrupts):**
- **RMT_CHn_TX_END_INTC (n = 0-3)**: Set this bit to clear RMT_CHn_TX_END_INT interrupt. (WT)
- **RMT_CHn_ERR_INTC_CLR (n = 0-3)**: Set this bit to clear RMT_CHn_ERR_INT interrupt. (WT)
- **RMT_CHn_TX_THR_EVENT_INTC (n = 0-3)**: Set this bit to clear RMT_CHn_TX_THR_EVENT_INT interrupt. (WT)
- **RMT_CHn_TX_LOOP_INTC (n = 0-3)**: Set this bit to clear RMT_CHn_TX_LOOP_INT interrupt. (WT)
- **RMT_CHm_RX_END_INTC (m = 4-7)**: Set this bit to clear RMT_CHm_RX_END_INT interrupt. (WT)
- **RMT_CHm_ERR_INTC_CLR (m = 4-7)**: Set this bit to clear RMT_CHm_ERR_INT interrupt. (WT)
- **RMT_CHm_RX_THR_EVENT_INTC (m = 4-7)**: Set this bit to clear the corresponding interrupt.
- **RMT_CH3_DMA_ACCESS_FAIL_INTC**: Set this bit to clear RMT_CH3_DMA_ACCESS_FAIL_INT interrupt. (WT)
- **RMT_CH7_DMA_ACCESS_FAIL_INTC**: Set this bit to clear RMT_CH7_DMA_ACCESS_FAIL_INT interrupt. (WT)

**Footer:**
Espressif Systems
1437 ESP32-S3 TRM (Version 1.7)