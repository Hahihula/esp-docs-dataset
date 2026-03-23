

```markdown
| Peripheral          | XTAL_CLK | APB_CLK | PLL_F160M_CLK | RTC_FAST_CLK | RC_FAST_CLK | CRYPTO_CLK | LEDC_CLK | PLL_D2_CLK |
|---------------------|:---------:|:--------:|:--------------:|:-------------:|:-----------:|:-----------:|:---------:|:-----------:|
| TIMG                |    Y      |    Y     |                |              |             |             |           |             |
| I2S                 |    Y      |          |       Y        |              |             |             |           |     Y       |
| UHCI                 |          |    Y     |                |              |             |             |           |             |
| UART                |    Y      |    Y     |                |              |      Y      |             |           |             |
| RMT                 |    Y      |    Y     |                |              |      Y      |             |           |             |
| I2C                 |    Y      |          |                |              |      Y      |             |           |             |
| SPI                 |    Y      |    Y     |                |              |             |             |           |             |
| eFuse Controller    |   ConY    |          |                |       Y       |             |             |           |             |
| SARADC              |          |    Y     |                |              |             |             |           |             |
| Temperature Sensor  |    Y      |          |                |              |      Y      |             |           |             |
| USB                 |          |    Y     |                |              |             |             |           |             |
| CRYPTO              |          |          |                |              |             |      Y      |           |             |
| TWAI Controller     |          |    Y     |                |              |             |             |           |             |
| LEDC                |    Y      |    Y     |       Y        |              |      Y      |             |     Y      |             |
| SYS_TIMER           |    Y      |    Y     |                |              |             |             |           |             |
```