

```markdown
Register 31.1. PCNT_Un_CONFO_REG (n: 0-3) (0x0000+0xC*n)

Continued from the previous page...

PCNT_CHO_LCTRL_MODE_Un Configures how the CHn_POS_MODE/CHn_NEG_MODE settings will be modified when the control signal is low.
O: No modification
1: Invert behavior (increase → decrease, decrease → increase)
2, 3: Inhibit counter modification
(R/W)

PCNT_CH1_NEG_MODE_Un Configures the behavior when the signal input of channel 1 detects a negative edge.
1: Increment the counter
2: Decrement the counter
O, 3: No effect
(R/W)

PCNT_CH1_POS_MODE_Un Configures the behavior when the signal input of channel 1 detects a positive edge.
1: Increment the counter
2: Decrement the counter
O, 3: No effect
(R/W)

PCNT_CH1_HCTRL_MODE_Un Configures how the CHn_POS_MODE/CHn_NEG_MODE settings will be modified when the control signal is high.
O: No modification
1: Invert behavior (increase → decrease, decrease → increase)
2, 3: Inhibit counter modification
(R/W)

PCNT_CH1_LCTRL_MODE_Un Configures how the CHn_POS_MODE/CHn_NEG_MODE settings will be modified when the control signal is low.
O: No modification
1: Invert behavior (increase → decrease, decrease → increase)
2, 3: Inhibit counter modification
(R/W)
```