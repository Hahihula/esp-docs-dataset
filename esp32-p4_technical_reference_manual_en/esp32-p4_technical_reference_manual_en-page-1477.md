

```markdown
Chapter 27 HMAC Accelerator (HMAC)

Register 27.15. HMAC_SET_MESSAGE_PAD_REG (0x00F0)
HM4AC_SET_TEXT_PAD

31
+-----------------------------+
| (reserved)                 |
+-----------------------------+
| HM4AC_SET_TEXT_PAD          | Reset
+-----------------------------+

HM4AC_SET_TEXT_PAD Configures whether or not the padding is applied by software.
O: Not applied by software
1: Applied by software
(WO)

Register 27.16. HMAC_ONE_BLOCK_REG (0x00F4)
HM4AC_SET_ONE_BLOCK

31
+-----------------------------+
| (reserved)                 |
+-----------------------------+
| HM4AC_SET_ONE_BLOCK         | Reset
+-----------------------------+

HM4AC_SET_ONE_BLOCK Write 1 to indicate there is only one block which already contains padding bits and there is no need for padding. (WO)

Register 27.17. HMAC_SOFT_JTAG_CTRL_REG (0x00F8)
HM4AC_SOFT_JTAG_CTRL

31
+-----------------------------+
| (reserved)                 |
+-----------------------------+
| HM4AC_SOFT_JTAG_CTRL        | Reset
+-----------------------------+

HM4AC_SOFT_JTAG_CTRL Configures whether or not to enable JTAG authentication mode.
O: Disable
1: Enable
(WO)
```