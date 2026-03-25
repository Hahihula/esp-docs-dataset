

```markdown
SOC_ETM_CHn_EVT_ID
SOC_ETM_CHn_TASK_ID

Figure 10.3-1. ETM Channel Architecture

SOC_ETM_CH_ENABLEn
SOC_ETM_CH_DISABLEn
SOC_ETM_CH_ENABLEDn

Events
MUX
Channel n
DEMux
Tasks

SOC_ETM_CHn_EVT_ID
SOC_ETM_CHn_TASK_ID

SOC_ETM_CHn_EVT_ID field configures the MUX (multiplexer) to select one of the events as the input of channeln.
The SOC_ETM_CHn_TASK_ID field configures the DEMUX (demultiplexer) to map the event selected by channeln to one of the tasks.

SOC_ETM_CH_ENABLEn and SOC_ETM_CH_DISABLEn are used to enable or disable channeln.
SOC_ETM_CH_ENABLEDn is used to indicate the status of the channeln.

10.3.2 Events

An ETM channel can be set up to select one event to receive by configuring the SOC_ETM_CHn_EVT_ID field.
Table 10.3-1 shows the configuration values of SOC_ETM_CHn_EVT_ID and their corresponding events.

Table 10.3-1. Selectable Events for ETM Channel

| SOC_ETM_CHn_EVT_ID | Selected Event                     | Peripheral Generating This Event |
|--------------------|------------------------------------|----------------------------------|
| 1                  | GPIO_EVT_CHO_RISE_EDGE             | GPIO                           |
| 2                  | GPIO_EVT_CH1_RISE_EDGE             |                                  |
| 3                  | GPIO_EVT_CH2_RISE_EDGE             |                                  |
| 4                  | GPIO_EVT_CH3_RISE_EDGE             |                                  |
| 5                  | GPIO_EVT_CH4_RISE_EDGE             |                                  |
| 6                  | GPIO_EVT_CH5_RISE_EDGE             |                                  |
| 7                  | GPIO_EVT_CH6_RISE_EDGE             |                                  |
| 8                  | GPIO_EVT_CH7_RISE_EDGE             |                                  |
| 9                  | GPIO_EVT_CHO_FALL_EDGE             |                                  |
| 10                 | GPIO_EVT_CH1_FALL_EDGE             |                                  |
| 11                 | GPIO_EVT_CH2_FALL_EDGE             |                                  |
```