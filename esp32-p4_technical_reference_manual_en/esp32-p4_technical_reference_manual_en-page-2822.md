

```markdown
outputs will continue until they are released by software. The events' triggers are configurable. They can be configured to be timing events or immediate events.

For NCI software-force events, set register `MCPWM_GENn_A_NCIFORCE` or `MCPWM_GENn_B_NCIFORCE` to 1 and then to 0 to trigger the NCI software-forced events of PWMxA or PWMxB. Configure register `MCPWM_GENn_A_NCIFORCE_MODE` or `MCPWM_GENn_B_NCIFORCE_MODE` to specify the operation on the PWMxA or PWMxB waveform when the NCI software-force event occurs. Configuring the registers to 0 or 3 means no operation, 1 means low level, and 2 means high level.

For CNTU software-force events, set register `MCPWM_GENn_CNTUFORCE_UMETHOD` to specify the trigger method of CNTU software-force events. Setting all bits to 0 means trigger CNTU software-force events immediately, setting bit 0 to 1 means the TEZ event triggers CNTU software-force events, setting bit 1 to 1 means the TEP event triggers CNTU software-force events, setting bit 2 to 1 means the TEA event triggers CNTU software-force events, setting bit 3 to 1 means the TEB event triggers CNTU software-force events, setting bit 4 to 1 means CNTU software-force events triggered when the PWM timer selected by the PWM generator is synchronized, and setting bit 5 to 1 means the CNTU software-forced events will not be triggered. Configure register `MCPWM_GENn_A_CNTUFORCE_MODE` or `MCPWM_GENn_B_CNTUFORCE_MODE` to specify the operation on the PWMxA or PWMxB waveform when the CNTU software-force events occur. Configuring the registers to 0 or 3 means no operation, 1 means low level, and 2 means high level.

Figure 56.3-19 shows a waveform of NCI software-force events. NCI events are used to force PWMxA output low. Forcing on PWMxB is disabled in this case.
```