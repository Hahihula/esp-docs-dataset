

```markdown
## Register 11.3. TIMG_TOHI_REG (0x0008)

TIMG_TO_HI After writing to TIMG_TOUPDATE_REG, the high 22 bits of the time-base counter of Timer 0 can be read here. (RO)


## Register 11.4. TIMG_TOUPDATE_REG (0x000C)

TIMG_TO_UPDATE After writing 0 or 1 to TIMG_TOUPDATE_REG, the counter value is latched. (R/W/SC)


## Register 11.5. TIMG_TOALARMLO_REG (0x0010)

TIMG_TO_ALARM_LO Timer 0 alarm trigger time-base counter value, low 32 bits. (R/W)


## Register 11.6. TIMG_TOALARMIHI_REG (0x0014)

TIMG_TO_ALARM_HI Timer 0 alarm trigger time-base counter value, high 22 bits. (R/W)
```