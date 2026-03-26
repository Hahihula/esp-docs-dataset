

```markdown
## Register 52.10. DMARINTWDTIMER_REG (0x1024)

RIWTC Configures the number of system clock cycles multiplied by 256.

The watchdog timer gets triggered with the programmed value after the RX DMA completes the transfer of a frame for which the RI (RECV_INT) status bit is not set because of the setting in the corresponding descriptor RDES1[31].

When the watchdog timer runs out, the RI bit is set and the timer is stopped. The watchdog timer is reset when the RI bit is set high because of the automatic setting of RI as per RDES1[31] of any received frame. (R/W)

## Register 52.11. DMAAHBSTATUS_REG (0x102C)

AHB_ST Configures the state of the AHB master interface.

0: Idle
1: Active
(R/W)

## Register 52.12. DMATXCURRDESC_REG (0x1048)

TRANS_DECR_ADDR_PTR Represents the address of the current transmit descriptor list updated by the DMA during operation.
This field is cleared on reset. (RO)
```