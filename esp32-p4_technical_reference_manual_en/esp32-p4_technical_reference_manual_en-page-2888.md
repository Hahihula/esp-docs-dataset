

```markdown
Chapter 57 Remote Control Peripheral (RMT)
GoBack

• The receiver supports:
    – Normal RX mode
    – Wrap RX mode
    – RX filtering
    – Demodulation on RX pulses
    – GDMA access supported by RX channel 7

57.3 Functional Description

57.3.1 Architecture

Figure 57.3-1. RMT Architecture

As shown in Figure 57.3-1, each TX channel has:
• 1 x clock divider counter (Div Counter)
• 1 x state machine (FSM)
• 1 x transmitter

Each RX channel has:
• 1 x clock divider counter (Div Counter)

Espressif Systems
2888
ESP32-P4 TRM
PRELIMINARY
Submit Documentation Feedback
```