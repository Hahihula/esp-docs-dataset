

Chapter 11 Low-Power Management  
GoBack

Register 11.60. PMU_POWER_PD_TOP_CNTL_REG (0x00F8)

| 31 | 27 | 26 | 11 | 10 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|----|---|---|---|---|---|---|---|
| 0  |    |    |    |    |   |   |   |   |   |   |   |
| Reset |

PMU_FORCE_TOP_RESET Configures whether or not to force reset "Peripherals+ROM" domain.  
0: No effect  
1: Force reset  
(R/W)

PMU_FORCE_TOP_ISO Configures whether or not to enable the force isolation of "Peripherals+ROM" domain. 0: No effect  
1: Enable  
(R/W)

PMU_FORCE_TOP_PU Configures whether or not to force power up "Peripherals+ROM" domain. This setting has a lower priority than PMU_PD_TOP_MASK.  
0: No effect  
1: Force power up  
(R/W)

PMU_FORCE_TOP_NO_RESET Configures whether or not to forcefully prevent the reset of "Peripherals+ROM" domain. This setting has a lower priority than PMU_FORCE_TOP_RESET.  
0: No effect  
1: Force not reset  
(R/W)

PMU_FORCE_TOP_NO_ISO Configures whether or not to disable the force isolation of "Peripherals+ROM" domain. This setting has a lower priority than PMU_FORCE_TOP_ISO.  
0: No effect  
1: Disable  
(R/W)

PMU_FORCE_TOP_PD Configures whether or not to force power down "Peripherals+ROM" domain. This setting has a lower priority than PMU_FORCE_TOP_PU.  
0: No effect  
1: Force power down  
(R/W)

Continued on the next page...