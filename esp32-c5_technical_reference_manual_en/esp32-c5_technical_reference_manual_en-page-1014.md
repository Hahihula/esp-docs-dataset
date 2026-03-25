

```markdown
Register 31.9. HUK_STATUS_REG (0x0034)

HUK_STATUS Represents the HUK generation status.
O: HUK is not generated.
1: HUK is generated and valid.
2: HUK is generated but invalid.
3: Reserved.
(RO)

HUK_RISK_LEVEL Represents the risk level of HUK.
0~6: The higher the risk level is, the more error bits there are in the PUF SRAM.
7: Error Level, HUK is invalid.
(RO)

HUK_UPDATE_REQ Represents the update request of huk_info.
O: User can update huk_info according to the risk level.
1: The huk_info is expired, and user need to update it.
(RO)

Register 31.10. HUK_DATE_REG (0x00FC)

HUK_DATE Version control register.
(R/W)
```

## 31.12.2 Key Manager Registers

The addresses in this section are relative to Key Manager base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section VII .
```