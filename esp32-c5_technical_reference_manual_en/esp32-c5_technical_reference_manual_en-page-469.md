

```markdown\n| JTAG Signal Source | eFuse 1² | eFuse 2³ | eFuse 3⁴ | GPIO7 |\n|:------------------------------------------------------------------------------------------------------------------|:----------|:----------|:----------|:-------|\n| USB Serial/JTAG Controller⁶ |           |           |           |        |\n| JTAG pins MTDI, MTK, MTMS, and MTDO | O         | x         | 1         | 0      |\n| USB Serial/JTAG Controller⁶ |           |           |           |        |\n| JTAG is disabled | 1         | x         | x         | x      |\n```

¹ Bold marks the default value and configuration.

² eFuse 1: EFUSE_DIS_PAD_JTAG

³ eFuse 2: EFUSE_DIS_USB_JTAG

⁴ eFuse 3: EFUSE_JTAG_SEL_ENABLE

⁵ x: x indicates that the value has no effect on the result and can be ignored.

⁶ In Joint Download Boot 1 mode, the USB Serial/JTAG controller is forcibly disabled, and the JTAG signal only comes from JTAG pins. If PAD_JTAG is also disabled, then JTAG is disabled.
```