

```markdown
Register 52.24. PMT_CSR_REG (0x002C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |
```

**RWKFILTRST** Configures whether to reset the RWKPTR register.  
- O: Release from reset  
- 1: Reset (R/WS/SC)

**RWKPTR** Configures the purpose of the PMT_RWUFFR register. For details, see the description of `PMT_RWUFFR`. (RO)

**GLBLUCAST** Configures whether to enable the unicast frame of target address filter as the wakeup frame.  
- O: Disable  
- 1: Enable (R/W)

**RWKPRCVD** Represents whether a remote wakeup frame event has been received.  
- O: Not received  
- 1: Received (R/SS/RC)

**MGKPRCVD** Represents whether a magic frame event has been received.  
- O: Not received  
- 1: Received (R/SS/RC)

**RWKPKTEN** Configures whether to enable power management events using remote wakeup frames.  
- O: Disable  
- 1: Enable (R/W)

**MGKPKTEN** Configures whether to enable power management events using magic frames.  
- O: Disable  
- 1: Enable (R/W)

**PWRDWN** Configures whether the EMAC receiver drops all received frames until it receives the expected magic frame or remote wakeup frame. Valid only when MGKPKTEN, GLBLUCAST or RWKPKTEN is 1. (R/WS/SC)
```