
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
PREP

PREP condition is satisfied and SPI_USR_COMMAND=1
CMD Condition is not satisfied
CMD

CMD condition is satisfied and SPI_USR_ADDR=1
ADDR Condition is not satisfied
ADDR

ADDR condition is satisfied and SPI_USR_DUMMY=1
DUMMY Condition is not satisfied
DUMMY

DONE Condition is satisfied
DONE

SPI_CS_HOLD=1
DONE Condition is not satisfied
IDLE

SPI_USR_CONF_NXT=1
SPI_CS_MISO=0
DIN Condition is not satisfied
DIN

SPI_CS_DUMMY=0
SPI_CS_MOSI=0
DOUT Condition is not satisfied
DOUT

SPI_USR_MISO=1
DUMMY Condition is not satisfied
DUMMY

SPI_USR_MOSI=1
DONE Condition is satisfied
DONE

Figure 28.5-5. GP-SPI2 State Machine as Master

Submit Documentation Feedback
837

ESP32-C6 TRM (Version 1.1)

Chapter 28 SPI Controller (SPI)
GoBack
```