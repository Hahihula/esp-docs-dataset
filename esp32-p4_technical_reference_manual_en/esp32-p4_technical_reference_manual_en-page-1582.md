

```markdown
Register 34.8. HUK_STATE_REG (0x0028)

HUK_STATE Represents the state of HUK Generator.

O: IDLE
1: LOAD
2: GAIN
3: BUSY
(RO)
```

```markdown
Register 34.9. HUK_STATUS_REG (0x0034)

HUK_STATUS Represents the HUK generation status.

O: HUK is not generated.
1: HUK is generated and valid.
2: HUK is generated but invalid.
3: Reserved.
(RO)

HUK_RISK_LEVEL Represents the risk level of HUK.

O~6: The higher the risk level is, the more error bits there are in the PUF SRAM.
7: Error Level, HUK is invalid.
(RO)

HUK_UPDATE_REQ Represents the update request of huk_info.

O: User can update huk_info according to the risk level.
1: The huk_info is expired, and user need to update it.
(RO)
```