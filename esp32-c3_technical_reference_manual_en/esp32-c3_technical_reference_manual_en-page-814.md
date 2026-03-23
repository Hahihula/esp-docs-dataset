

# 31.6 Registers

'|' here means separate line. The left describes the access in Operation Mode. The right belongs to Reset Mode with red color. The addresses in this section are relative to Two-wire Automotive Interface base address provided in Table 3.3-3 in Chapter 3 System and Memory.

## Register 31.1. TWAI_MODE_REG (0x0000)

```
31 | 4 3 2 1 0
+---+-----+-----+-----+-----+
|   |TWAI_RX_FILTER_MODE|TWAI_SELF_TEST_MODE|TWAI_LISTEN_ONLY_MODE|TWAI_RESET_MODE|
+---+---------------------+---------------------+---------------------+---------------+
```

- **TWAI_RESET_MODE** This bit is used to configure the operation mode of the TWAI Controller. 1: Reset mode; 0: Operation mode (R/W)
- **TWAI_LISTEN_ONLY_MODE** 1: Listen only mode. In this mode the nodes will only receive messages from the bus, without generating the acknowledge signal nor updating the RX error counter. (R/W)
- **TWAI_SELF_TEST_MODE** 1: Self test mode. In this mode the TX nodes can perform a successful transmission without receiving the acknowledge signal. This mode is often used to test a single node with the self reception request command. (R/W)
- **TWAI_RX_FILTER_MODE** This bit is used to configure the filter mode. 0: Dual filter mode; 1: Single filter mode (R/W)

## Register 31.2. TWAI_BUS_TIMING_O_REG (0x0018)

```
31 | 16   15   14   13   12    0
+---+-----------------------------+
|   |TWAI_SYNC_JUMP_WIDTH|reserved|TWAI_BAUD_PRESC|
+---+-----------------------------+
```

- **TWAI_BAUD_PRESC** Baud Rate Prescaler value, determines the frequency dividing ratio. (RO | R/W)
- **TWAI_SYNC_JUMP_WIDTH** Synchronization Jump Width (SJW), 1 ~ 14 Tq wide. (RO | R/W)