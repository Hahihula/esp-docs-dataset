
```markdown
Espressif Systems

SPI_USR=0
IDLE

SPI_USR=1 & SPI_USR_CONF=1
CONF Condition is not satisfied
SPI_USR_CONF=0
CONF

CONF condition is satisfied and SPI_CS_SETUP=1
PREP Condition is not satisfied
SPI_CS_SETUP=0
PREP

PREP condition is satisfied and SPI_USR_COMMAND=1
CMD Condition is not satisfied
SPI_USR_COMMAND=0
CMD

CMD condition is satisfied and SPI_USR_ADDR=1
ADDR Condition is not satisfied
SPI_CS_DUMMY=0
ADDR

ADDR condition is satisfied and SPI_LUSR_DUMMY=1
DUMMY Condition is not satisfied
SPI_USR_MOSI=1
DUMMY

DONE Condition is satisfied
SPI_CS_HOLD=1
DONE

DONE Condition is not satisfied
IDLE

SPI_USR_CONF_NXT=1
SPI_CS_MISO=0
DIN Condition is not satisfied
DIN

DOUT Condition is not satisfied
SPI_USR_MISO=1
DOUT

DUMMY Condition is not satisfied
SPI_USR_MOSI=1
DUMMY

DIN condition is satisfied
DONE

DOUT condition is satisfied and SPI_USR_MISO=1
DONE

Figure 33.5-5. GP-SPI2 State Machine
```