

```markdown
Espressif Systems

SPI_USR=0
IDLE → (DONE Condition is satisfied) DONE

SPI_USR=1 & SPI_USR_CONF=1
IDLE → CONF (CONF Condition is not satisfied)
→ (SPI_USR_CONF=0, SPI_USR_CONF_NXT=1) IDLE or DIN?

CONF → PREP (PREP Condition is not satisfied)
→ (SPI_CS_MISO=0) DIN

PREP → CMD (CMD Condition is not satisfied)
→ (SPI_USR_COMMAND=0) ADDR

CMD → ADDR (ADDR Condition is not satisfied)
→ (SPI_USR_ADDR=1) DUMMY

ADDR → DUMMY (ADDR condition is satisfied and SPI_USR_DUMMY=1)
→ (SPI_CS_DUMMY=0) DOUT or DIN?

DUMMY → DOUT (DUMMY Condition is not satisfied)
→ (SPI_USR_MOSI=1) ADDR

DIN → DONE (DONE Condition is satisfied)
→ (SPI_CS_HOLD=1)

DOUT → DONE (DONE Condition is not satisfied)

Legend to state flow:

- Orange dashed line: indicates corresponding state condition is not satisfied; repeats current state.
- Blue solid line: corresponding registers are set and conditions are satisfied; goes to next state.
- Red solid line: state registers are not set; skips one or more following states, depending on whether the registers of the following states are set or not.

Figure 26.5-5. GP-SPI2 State Machine

Submit Documentation Feedback
894
ESPS32-C61 TRM (Pre-release v0.5)
PRELIMINARY
Chapter 26 SPI Controller (SPI)
GoBack
```