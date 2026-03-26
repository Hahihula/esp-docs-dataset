

```markdown
| Derived Clock | RC_FAST_CLK | XTAL_CLK | CPLK | MPLL_CLK | SPLK | APLL_CLK | SDIO_PLO_CLK | ROOT_CLK | CPU_CLK | MEM_CLK | SYS_CLK | PLL_F30M_CLK | PLL_F160M_CLK | PLL_F240M_CLK |
|---------------|-------------|----------|------|----------|------|----------|--------------|----------|---------|---------|---------|--------------|----------------|----------------|
| ROOT_CLK      | Y           | Y        | Y    |          |      |          |              |          |         |         |         |              |                |                |
| CPU_CLK       |             |          |      |          |      |          |              |          | Y       |         |         |              |                |                |
| MEM_CLK       |             |          |      |          |      |          |              |          |         | Y       |         |              |                |                |
| SYS_CLK       |             |          |      |          |      |          |              |          |         |         | Y       |              |                |                |
| APB_CLK       |             |          |      |          |      |          |              |          |         |         |         | Y            |                |                |
| PLL_F50M_CLK  |             |          |      |          |      |          |              |          |         |         |         |              | Y              |                |
| PLL_F25M_CLK  |             |          |      |          |      |          |              |          |         |         |         |              |                | Y              |
| PLL_F240M_CLK |             |          |      |          |      |          |              |          |         |         |         |              |                | Y              |
| PLL_F160M_CLK |             |          |      |          |      |          |              |          |         |         |         |              | Y              |                |
| PLL_F120M_CLK |             |          |      |          |      |          |              |          |         |         |         |              |                | Y              |
| PLL_F80M_CLK  |             |          |      |          |      |          |              |          |         |         |         |              |                | Y              |
| PLL_F48M_CLK  |             |          |      |          |      |          |              |          |         |         |         |              |                | Y              |
| FLASH_CLK     |             |          | Y    |          |      |          |              |          |         |         |         |              |                |                |
| PSRAM_CLK     |             |          | Y    |          |      |          |              |          |         |         |         |              |                |                |
| GPSPI_CLK     |             |          | Y    |          | Y    |          |              |          |         |         |         |              |                |                |
| ADC_CLK       |             |          | Y    |          |      |          |              |          |         |         |         | Y            |                |                |
| UART_CLK      |             |          | Y    |          |      |          |              |          |         |         |         | Y            |                |                |
| CRYPTO_CLK    |             |          | Y    |          |      |          |              |          |         |         |         | Y            |                |                |

Table 10.2-5. HP Peripheral Clocks
```