

```markdown
cycles.

## 13.3.6 Channel Control

Each ETM channel can be independently configured to be enabled or disabled. When channel`n` is enabled and receives the event configured via `SOC_ETM_CHn_EVT_ID`, it maps the event to the task configured via `SOC_ETM_CHn_TASK_ID`. When channel`n` is disabled, even if it receives the event configured via `SOC_ETM_CHn_EVT_ID`, no task will be generated.

To enable ETM channel`n`, write 1 to `SOC_ETM_CH_ENABLEn`. To disable ETM channel`n`, Write 1 to `SOC_ETM_CH_DISABLEn`.

The status of ETM channel`n` can be obtained by reading `SOC_ETM_CH_ENABLEDn`. 1 indicates that channel`n` has been enabled, and 0 indicates disabled.

If `SOC_ETM_CHn_EVT_ID` or `SOC_ETM_CHn_TASK_ID` is configured to 0, ETM channel`n` will also be disabled.

The complete procedure to configure ETM channel`n` is as follows:

1. Enable the ETM’s clock by writing 1 to HP_SYS_CLKRST_REG_ETM_SYS_CLK_EN
2. Select the event to be received by channel`n` via `SOC_ETM_CHn_EVT_ID`
3. Select the task mapped to the received event via `SOC_ETM_CHn_TASK_ID`
4. Enable channel`n` by setting `SOC_ETM_CH_ENABLEn`
5. When channel`n` no longer needs to map the selected event to the selected task, disable channel`n` by setting `SOC_ETM_CH_DISABLEn`. To configure a new event and task mapping, repeat Steps 2 to 4. If no configurations, channel`n` will remain disabled
6. The whole ETM module (i.e., all ETM channels) can be reset by writing 1 and then 0 to the `HP_SYS_CLKRST_REG_RST_EN_ETM` field
```