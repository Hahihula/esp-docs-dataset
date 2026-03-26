
```markdown
Espressif Systems

SPI_USR=0                          SPI_USR=1 & SPI_USR_CONF=1                 CONF condition is satisfied and SPI_CS_SETUP=1          PREP condition is satisfied and SPI_USR_COMMAND=1           CMD condition is satisfied and SPI_USR_ADDR=1            ADDR condition is satisfied and SPI_LUSR_DUMMY=1
IDLE  ────────────────────────────────► CONF ─────────────────────────────────────────► PREP ─────────────────────────────────────────► CMD ─────────────────────────────────────────► ADDR

CONF Condition is not satisfied   PREP Condition is not satisfied    CMD Condition is not satisfied     ADDR Condition is not satisfied
SPI_USR_CONF=0                   SPI_CS_SETUP=0                    SPI_USR_COMMAND=0                  SPI_CS_ADDR=0

DONE Condition is satisfied       SPI_USR_CONF_NXT=1                 SPI_CS_MISO=0                      SPI_CS_DUMMY=0
IDLE ────────────────────────────────► DONE ─────────────────────────────────────────► DIN ─────────────────────────────────────────► DOUT ─────────────────────────────────────────► DUMMY

DONE Condition is not satisfied    DIN Condition is not satisfied       DOUT Condition is not satisfied     DUMMY Condition is not satisfied
SPI_CS_HOLD=1                     SPI_USR_MOSI=0                      SPI_USR_MISO=1                      SPI_USR_MOSI=1

Figure 43.5-5. GP-SPI State Machine as Master
```