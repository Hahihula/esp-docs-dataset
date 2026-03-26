

```markdown
| Internal Interrupt Source | Trigger Condition                  | Interrupt Signal |
|----------------------------|-------------------------------------|------------------|
| MB_HP_m_INT               | Write to MB_MESSAGE_m_REG          | MB_HP_INTR      |
| MB_LP_n_INT               | Write to MB_MESSAGE_n_REG          | MB_LP_INTR      |

**Note:**
*   `m` and `n` can be 0 ~ 15.
*   MB_HP_INTR can also serve as an external interrupt source for LP CPU and be mapped to LP CPU by LP_INTR_MAP as illustrated in Figure 22.3-1. For more information about LP_INTR_MAP, please refer to Chapter 3 Low-Power CPU.
*   MB_LP_INTR can also serve as an external interrupt source for HP CPUx and can be mapped to HP CPUx through the Interrupt Matrix.
*   When the LP Mailbox is required to assign different interrupt sources for HP CPU0 and HP CPU1, it can map MB_HP_INTR and MB_LP_INTR independently to HP CPU0 and HP CPU1 using the Interrupt Matrix.

## 22.3.3 Inter-Core Communication

When communication is required between LP CPU and HP CPUx, subset of or all message registers in the LP Mailbox can be utilized to share message as needed. The synchronization of message can be achieved through the corresponding interrupts. During communication, software must ensure that only the sender is allowed to write to the message registers to prevent data corruption.

*   Example of initiating communication from HP CPU0 to LP CPU using MB_MESSAGE_n_REG:
    -   Set `MB_LP_n_INT_ENA` to enable the `MB_LP_n_INT` interrupt.
    -   HP CPU0 writes to `MB_MASSEGE_n_REG`, caching shared message.
    -   LP CPU checks `MB_LP_INT_ST_REG` interrupt status register, finding the `MB_LP_n_ST` status bit set.
    -   LP CPU reads `MB_MASSEGE_n_REG` to retrieve shared message.

*   Example of initiating communication from LP CPU to HP CPU0:
    -   Set `MB_HP_m_INT_ENA` to enable the `MB_HP_m_INT` interrupt.
    -   Configure the Interrupt Matrix to map MB_HP_INTR to HP CPU0. See Chapter 12 Interrupt Matrix.
    -   LP CPU writes to `MB_MASSEGE_m_REG`, caching shared messages.
    -   HP CPU0 checks the `MB_HP_INT_ST_REG` interrupt status register, finding the `MB_HP_m_ST` status bit set.
    -   HP CPU0 reads `MB_MASSEGE_m_REG` to retrieve shared messages.
```