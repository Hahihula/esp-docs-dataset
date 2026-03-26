

```markdown
| Parameters                     | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Description                                                                 |
|---------------------------------|---------:|------------------------:|---------------------------------------------:|------------------------------------------------------------------------------|
| EFUSE_OPXA_TIEH_SEL2            |      2   |              Y          |                                            2 | Represents which output source is used for Extern Power (VO3).               |
| EFUSE_OPXA_TIEH_SEL3            |      2   |              Y          |                                            2 | Represents which output source is used for Extern Power (VO4).               |
| EFUSE_HP_PWR_SRC_SEL           |      1   |              Y          |                                            3 | Represents the HP system power source.                                       |
| EFUSE_DCDC_VSET_EN             |      1   |              Y          |                                             N/A | Represents whether to use the default voltage configured by EFUSE_DCDC_VSET. |
| EFUSE_DIS_WDT                  |      1   |              Y          |                                            2 | Represents whether to disable the watchdog.                                   |
| EFUSE_DIS_SWD                  |      1   |              Y          |                                            2 | Represents whether to disable the super watchdog.                            |
```