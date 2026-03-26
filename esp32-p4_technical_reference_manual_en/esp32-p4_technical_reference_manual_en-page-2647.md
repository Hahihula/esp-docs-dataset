

```markdown
|31|30|(reserved)|SAIRC|ASS2KP (reserved)|EMACCORC_STRIP (reserved)|EMACWATCHDOG (reserved)|EMACJABBER (reserved)|EMACJUMBOMFRAME|EMACINTERFRAME GAP|EMACDISABLELCRS|EMACMII|EMACOFFERSPEED|EMACLOOPBACK|EMACCRXPLCP|EMACRXPCFLOP|EMACPAADCRCSTRIP (reserved)|EMACBACKOFFLIMIT|EMACDEFERRALCHECK|EMACTX|EMACRX|PLTF|
|---|---|-----------|------|------------------|--------------------------|-------------------------|-----------------------|-----------------|-------------------|---------------|--------|--------------|-------------|------------|------------|----------------------------|-----------------|--------------------|-------|-------|-----|
|0x0|0x0|           |      |                  |                          |                         |                       |                 |                   |               |        |              |             |            |            |                            |                 |                    |       |       |     |
```

**Register 52.16. EMACCONFIG_REG (0x0000)**

**SAIRC** Configures the source address insertion or replacement for all transmitted frames.
Bit 30 specifies which MAC Address register (0 or 1) is used for source address insertion or replacement based on the values of Bits [29:28].

Bits [29:28]:
O, 1: The input mti_sa_ctrl_i and ati_sa_ctrl_i control the SA field generation
2: Insert the content of the MAC Address register (0 or 1) in the SA field of all transmitted frames
3: Replace the content of MAC Address register (0 or 1) in the SA field of all transmitted frames

Bit 30:
O: Use MAC Address 0 register
1: Use MAC Address 1 register
(R/W)

**ASS2KP** Configures whether the MAC considers received frames of more than 2000 bytes as normal packets or giant frames.
O: Giant frames. In this case, if Bit[20] (JE) is 0, the MAC considers all received frames of size more than 1,518 bytes (1,522 bytes for tagged) as Giant frames.
1: Normal packets.
(R/W)

**EMACCRC_STRIP** Configures whether to strip and drop the last 4 bytes (FCS) of all frames of Ether type (Length/Type field greater than or equal to 1,536) before forwarding the frame to the application.

O: Not strip and drop
1: Strip and drop
(R/W)

**EMACWATCHDOG** Configures whether to disable the watchdog timer.
O: Enable. In this case, the MAC does not allow a receive frame with more than 2,048 bytes (10,240 if JE is set high) or the value programmed in Watchdog Timeout Register. The MAC cuts off any bytes received after the watchdog limit number of bytes.
1: Disable. In this case, the MAC can receive frames of up to 16,384 bytes.
(R/W)

**EMACJABBER** Configures whether to disable the jabber timer on the transmitter.
O: Enable. In this case, the MAC cuts off the transmitter if the application sends out more than 2,048 bytes of data (10,240 if JE is set high) during transmission.
1: Disable. In this case, the MAC can transfer frames of up to 16,384 bytes.
(R/W)
```