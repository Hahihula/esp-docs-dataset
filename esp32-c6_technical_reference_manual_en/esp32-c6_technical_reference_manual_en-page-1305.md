

```markdown
# 37.3 Functional Description

## 37.3.1 RMT Architecture

Figure 37.3-1. RMT Architecture

As shown in Figure 37.3-1, each TX channel has:
*   1 x clock divider counter (Div Counter)
*   1 x state machine (FSM)
*   1 x transmitter

Each RX channel also has:
*   1 x clock divider counter (Div Counter)
*   1 x state machine (FSM)
*   1 x receiver

The four channels share a 192 x 32-bit RAM.
```