

```markdown
Register 52.50. EMACTSTPCTRL_REG (0x0700)

Continued from the previous page...

TSTRIG Configures whether to enable the timestamp interrupt trigger.
O: Disable
1: Enable. The timestamp interrupt is generated when the System Time becomes greater than the value written in the Target Time register (R/WS/SC)

TSUPDT Configures whether to update (add or subtract) the system time with the value specified in EMAC2NDUPT_REG and EMACNSUPT_REG.
O: Not update
1: Update
This bit should be read as zero before updating it.
EMACSYSSTIMHIGHWORD2ND_REG is not updated. (R/WS/SC)

TSINIT Configures whether to initialize (overwrite) the system time with the value specified in EMAC2NDUPT_REG and EMACNSUPT_REG.
O: Not initialize
1: Initialize
This bit should be read as zero before updating it.
EMACSYSSTIMHIGHWORD2ND_REG will be initialized. (R/WS/SC)

TSCFUPDT Configures the method used to update the system time.
O: Coarse method
1: Find update method
(R/W)

TSENA Configures whether to add the timestamp for the transmit and receive frames.
O: Not add the timestamp, and receive frames and the Timestamp Generator is also suspended
1: Add the timestamp
You need to initialize the Timestamp (system time) after setting this bit to 1.
On the receive side, the MAC processes the 1588 frames only if this bit is set. (R/W)
```