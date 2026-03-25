

Chapter 8 GPIO Matrix and IO MUX  
GoBack  

Register 8.37. GPIO_EXT_ETM_TASK_P5_CFG_REG (0x016C)  

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) |    |    |    |    |    |    | GPIO_EXT_ETM_TASK_GPIO28_EN<br>(reserved) |    |    |    | GPIO_EXT_ETM_TASK_GPIO28_SEL<br>(reserved) |    |    | GPIO_EXT_ETM_TASK_GPIO27_EN<br>(reserved) |    |    | GPIO_EXT_ETM_TASK_GPIO27_SEL<br>(reserved) |    |    | GPIO_EXT_ETM_TASK_GPIO26_EN<br>(reserved) |    |    | GPIO_EXT_ETM_TASK_GPIO26_SEL<br>(reserved) |    |    | GPIO_EXT_ETM_TASK_GPIO25_SEL<br>(reserved) |    |    | Reset |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

GPIO_EXT_ETM_TASK_GPIO25_SEL Configures to select an ETM task channel for GPIO25.  
0: Select channel 0  
1: Select channel 1  
......  
7: Select channel 7  
(R/W)  

GPIO_EXT_ETM_TASK_GPIO25_EN Configures whether or not to enable GPIO25 to response ETM task.  
0: Not enable  
1: Enable  
(R/W)  

GPIO_EXT_ETM_TASK_GPIO26_SEL Configures to select an ETM task channel for GPIO26.  
0: Select channel 0  
1: Select channel 1  
......  
7: Select channel 7  
(R/W)  

GPIO_EXT_ETM_TASK_GPIO26_EN Configures whether or not to enable GPIO26 to response ETM task.  
0: Not enable  
1: Enable  
(R/W)  

GPIO_EXT_ETM_TASK_GPIO27_SEL Configures to select an ETM task channel for GPIO27.  
0: Select channel 0  
1: Select channel 1  
......  
7: Select channel 7  
(R/W)  

GPIO_EXT_ETM_TASK_GPIO27_EN Configures whether or not to enable GPIO27 to response ETM task.  
0: Not enable  
1: Enable  
(R/W)  

Continued on the next page...