

```markdown
|31|28|27|26|25|24|23|22|21|20|17|16|15|12|11|10|9|8|7|6|5|4|3|2|1|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
|0|0|0|0|0|1|0|0|0| |0x0|0|0|0|0|0|0|1|0|0|0|0|1|0|0|0|Reset|

TWAIFD_RST Configures whether to soft reset. Writing 1 resets CAN FD. After writing 1, there is no need to write 0, as this field will be automatically cleared.
O: Invalid
1: Reset (WO)

TWAIFD_BMM Configures whether to enable the bus monitoring mode.
O: Disable
1: Enable (R/W)

TWAIFD_STM Configures whether to enable the self test mode.
O: Disable
1: Enable (R/W)

TWAIFD_AFM Configures whether to enable the acceptance filter mode.
O: Disable
1: Enable (R/W)

TWAIFD_FDE Configures whether to enable the flexible data rate enable. When enabled, CAN FD recognizes CAN FD frames (FDF bit = 1).
O: Disable
1: Enable (R/W)

TWAIFD_TTTM Configures whether to enable the time triggered transmission mode.
O: Disable
1: Enable (R/W)

TWAIFD_ROM Configures whether to enable the restricted operation mode.
O: Disable
1: Enable (R/W)

TWAIFD_ACF Configures whether to enable the acknowledge forbidden mode.
O: Disable
1: Enable (R/W)
```