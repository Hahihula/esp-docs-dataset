

```markdown
## 34.5.6 SDIO Bus Timing

The SDIO bus operates at a very high speed and the PCB trace length usually affects signal integrity by introducing latency. To ensure that the timing characteristics conform to the desired bus timing, the SDIO slave module supports configuration of input sampling clock edge and output driving clock edge.

When the incoming data changes near the rising edge of the clock, the slave will perform sampling on the falling edge of the clock, or vice versa, as Figure 34.5-8 shows.

Figure 34.5-8. Sampling Timing Diagram

By default, the MTMS (GPIO4) strapping value determines the slave’s sampling edge. However, users can decide the sampling edge by configuring the SLCHOST_CONF_REG register, with priority from high to low:  
(1) Set SLCHOST_FRC_POS_SAMP to sample the corresponding signal at the rising edge;  
(2) Set SLCHOST_FRC_NEG_SAMP to sample the corresponding signal at the falling edge.

SLCHOST_FRC_POS_SAMP and SLCHOST_FRC_NEG_SAMP fields are five bits wide. The bits correspond to the CMD line and four DATA lines (0-3). Setting a bit causes the corresponding line to be sampled for input at the rising clock edge or falling clock edge.

The slave can also select which edge to drive the output lines, in order to accommodate for any latency caused by the physical signal path. The output timing is shown in Figure 34.5-9.

Figure 34.5-9. Output Timing Diagram

By default, the MTDI (GPIO5) strapping value determines the slave’s output driving edge. However, users can decide the output driving edge by configuring the following registers, with priority from high to low:  
(1) Set SLCHOST_FRC_SDIO11 in SLCHOST_CONF_REG to output the corresponding signal at the falling clock edge;  
(2) Set SLCHOST_FRC_SDIO22 in SLCHOST_CONF_REG to output the corresponding signal at the rising clock edge;  
(3) Set HINF_HIGHSPEED_ENABLE in HINF_CFG_DATA1_REG and SLCHOST_HSPEED_CON_EN in SLCHOST_CONF_REG, then set the EHS (Enable High-Speed) bit in CCCR at the host side to output the corresponding signal at the rising clock edge.

SLCHOST_FRC_SDIO11 and SLCHOST_FRC_SDIO22 fields are five bits wide. The bits correspond to the CMD line and four DATA lines (0-3). Setting a bit causes the corresponding line to output at the rising clock edge or falling clock edge.
```