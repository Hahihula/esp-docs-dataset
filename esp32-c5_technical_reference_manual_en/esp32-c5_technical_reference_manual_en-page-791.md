

```markdown
## 18.9.5 TEE_REG

The addresses in this section are relative to the TEE base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 18.73. TEE_Mn_MODE_CTRL_REG (n: 0-31) (0x0000+0x4*n)

| Bit 31 | ... | 2 | 1 | 0 |
|--------|-----|---|---|---|
|        |     |   |   | Reset |

TEE_Mn_MODE Configures the security mode for master n.
0: TEE
1: REE0
2: REE1
3: REE2
(R/W)

TEE_Mn_LOCK Configures whether to lock the value of TEE_Mn_MODE.
0: Do not lock
1: Lock
(R/W)

Register 18.74. TEE_UART0_CTRL_REG (0x0088)
Register 18.75. TEE_UART1_CTRL_REG (0x008C)
Register 18.76. TEE_UHCIO_CTRL_REG (0x0090)
Register 18.77. TEE_I2C_EXT0_CTRL_REG (0x0094)
Register 18.78. TEE_I2S_CTRL_REG (0x009C)
Register 18.79. TEE_PARL_IO_CTRL_REG (0x00AO)
Register 18.80. TEE_PWM_CTRL_REG (0x00A4)
Register 18.81. TEE_LEDC_CTRL_REG (0x00AC)
Register 18.82. TEE_TWAIO_CTRL_REG (0x00B0)
Register 18.83. TEE_USB_SERIAL_JTAG_CTRL_REG (0x00B4)
Register 18.84. TEE_RMT_CTRL_REG (0x00B8)
Register 18.85. TEE_GDMA_CTRL_REG (0x00BC)
Register 18.86. TEE_ETM_CTRL_REG (0x00C4)
Register 18.87. TEE_INTMTX_CTRL_REG (0x00C8)
Register 18.88. TEE_APP_ADC_CTRL_REG (0x00DO)
```