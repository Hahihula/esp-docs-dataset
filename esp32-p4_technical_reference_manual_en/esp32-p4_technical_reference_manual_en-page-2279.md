

```markdown
Register 43.16. SPI_DOUT_MODE_REG (0x002C)
```

| bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    | SPI_DQ5_MODE | SPI_DOUT7_MODE | SPI_DOUT6_MODE | SPI_DOUT5_MODE | SPI_DOUT4_MODE | SPI_DOUT3_MODE | SPI_DOUT2_MODE | SPI_DOUT1_MODE | SPI_DOUT0_MODE | Reset |

---

**SPI_DOUT0_MODE** Configures the output mode for SPI2D signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

---

**SPI_DOUT1_MODE** Configures the output mode for SPI2Q signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

---

**SPI_DOUT2_MODE** Configures the output mode for SPI2WP signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

---

**SPI_DOUT3_MODE** Configures the output mode for SPI2HD signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

---

**SPI_DOUT4_MODE** Configures the output mode for SPI2D4 signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

---

**SPI_DOUT5_MODE** Configures the output mode for SPI2D5 signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)

---

**SPI_DOUT6_MODE** Configures the output mode for SPI2D6 signal.  
0: Output without delay  
1: Output with a delay of a SPI module clock cycle at its falling edge  
Can be configured in CONF state.  
(R/W)
```