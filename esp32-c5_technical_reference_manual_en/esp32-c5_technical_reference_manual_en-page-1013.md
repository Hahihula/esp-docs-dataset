

```markdown
Chapter 31 Key Manager

Register 31.6. HUK_CONF_REG (0x0020)

HUK_MODE Configures HUK mode.
O: HUK Recovery Mode
1: HUK Generation Mode
(R/W)

Register 31.7. HUK_START_REG (0x0024)

HUK_START Write 1 to start HUK Generator at IDLE phase.
(WT)

HUK_CONTINUE Write 1 to continue HUK Generator operation at LOAD/GAIN phase.
(WT)

Register 31.8. HUK_STATE_REG (0x0028)

HUK_STATE Represents the state of HUK Generator.
O: IDLE
1: LOAD
2: GAIN
3: BUSY
(RO)
```