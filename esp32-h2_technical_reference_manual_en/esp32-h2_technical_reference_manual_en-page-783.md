
```markdown
Espressif Systems

SPI_USR=0
IDLE -> (DONE Condition is satisfied) DONE

SPI_USR=1 & SPI_USR_CONF=1
IDLE -> CONF (CONF Condition is not satisfied)
CONF -> PREP (PREP Condition is not satisfied)

CONF condition is satisfied and SPI_CS_SETUP=1
PREP -> CMD (CMD Condition is not satisfied)

PREP condition is satisfied and SPI_USR_COMMAND=1
CMD -> ADDR (ADDR Condition is not satisfied)

ADDR condition is satisfied and SPI_USR_ADDR=1
ADDR -> DUMMY (DUMMY Condition is not satisfied)

ADDR condition is satisfied and SPI_USR_DUMMY=1
ADDR -> DUMMY

DONE Condition is satisfied
DONE <- IDLE (via DONE Condition is satisfied)
DONE <- CONF (SPI_USR_CONF_NXT=1)
DONE <- PREP (SPI_CS_MISO=0)
DONE <- CMD (SPI_CS_MOSI=0)
DONE <- DIN (DIN Condition is satisfied)
DONE <- DOUT (DOUT Condition is satisfied and SPI_USR_MISO=1)

Dummy transitions:
ADDR -> DUMMY
DUMMY -> (DUMMY Condition is not satisfied) back to ADDR or other states as per conditions.

Transitions with specific signals:
SPI_USR_CONF=0 from CONF state leads potentially toward DONE via SPI_USR_CONF_NXT=1.
SPI_CS_HOLD=1 causes DONE condition check failure, leading out of DONE if not met (loopback implied).
SPI_CS_DUMMY=0 transition affects CMD to DOUT path.

State Machine States:
- IDLE
- CONF
- PREP
- CMD
- ADDR
- DUMMY
- DIN
- DOUT
- DONE

Conditions for transitions between states are detailed with SPIUSR signals and setup/dummy conditions.
```