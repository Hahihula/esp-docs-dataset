

```markdown
Register 19.9. AES_TRIGGER_REG (0x0048)

31 | [reserved] | AES_TRIGGER
---|------------|-----------
  |            |   1    0
0x00000000 | x Reset


AES_TRIGGER Configures whether or not to start AES operation.
O: No effect
1: Start
(WO)


Register 19.10. AES_STATE_REG (0x004C)

31 | [reserved] | AES_STATE
---|------------|-----------
  |            |   2    1    0
0x00000000 | 0x0 Reset


AES_STATE Represents the working status of the AES accelerator.
In Typical AES working mode:
O: IDLE
1: WORK
2: No effect
3: No effect

In DMA-AES working mode:
O: IDLE
1: WORK
2: DONE
3: No effect
(RO)
```