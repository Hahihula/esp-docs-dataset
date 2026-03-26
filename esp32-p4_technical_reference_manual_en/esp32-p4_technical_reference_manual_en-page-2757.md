

```markdown
Register 54.17. SDHOST_RST_N_REG (0x0078)
```

| Bit | Description |
|-----|-------------|
| 31-2 | (reserved) |
| 1    | SDHOST_CARD_RESET<br>Configures hardware reset per card. Bit[0] corresponds to card[0]. These bits cause the cards to enter the pre-idle state, which requires them to be re-initialized. For every card bit:<br>0: Reset<br>1: Active mode (R/W) |

```markdown
Espressif Systems 2757 ESP32-P4 TRM PRELIMINARY Submit Documentation Feedback
```