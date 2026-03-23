
```markdown
Espressif Systems

SPI_USR=0
IDLE -> (DONE Condition is satisfied) DONE

SPI_USR=1 & SPI_USR_CONF=1
IDLE -> CONF (CONF Condition is not satisfied)
CONF -> PREP (PREP Condition is not satisfied)

PREP -> CMD (CMD Condition is not satisfied)

CMD -> ADDR (ADDR Condition is not satisfied)

ADDR -> DUMMY (ADDR condition is satisfied and SPI_LUSR_DUMMY=1 & SPI_CS_DUMMY=0)

DUMMY -> DOUT (DUMMY Condition is not satisfied)
DOUT -> DIN (DIN Condition is not satisfied)
DIN -> DONE (DONE Condition is satisfied)

DONE -> IDLE (DONE Condition is not satisfied, SPI_CS_HOLD=1)

SPI_USR_CONF=0
CONF <- SPI_USR_CONF_NXT=1

SPI_CS_MISO=0
PREP <- SPI_CS_SETUP=0

SPI_USR_COMMAND=0
CMD <- SPI_USR_COMMAND=1

SPI_USR_ADDR=1
ADDR <- SPI_CS_ADDR=0

SPI_USR_MOSI=1
DUMMY <- SPI_USR_MOSI=1

DONE Condition is satisfied
IDLE -> DONE

CONF Condition is not satisfied
IDLE -> CONF

PREP Condition is not satisfied
CONF -> PREP

CMD Condition is not satisfied
PREP -> CMD

ADDR Condition is not satisfied
CMD -> ADDR

DUMMY Condition is not satisfied
ADDR -> DUMMY

DIN Condition is not satisfied
DUMMY -> DIN

DONE Condition is satisfied
DIN -> DONE

SPI_USR_CONF_NXT=1
CONF <- SPI_USR_CONF_NXT=1

SPI_CS_MISO=0
PREP <- SPI_CS_MISO=0

SPI_USR_COMMAND=0
CMD <- SPI_USR_COMMAND=0

SPI_USR_ADDR=1
ADDR <- SPI_USR_ADDR=1

SPI_USR_MOSI=1
DUMMY <- SPI_USR_MOSI=1

DONE Condition is not satisfied, SPI_CS_HOLD=1
DONE -> IDLE

Figure 27.5-5. GP-SPI2 State Machine in Master Mode
```