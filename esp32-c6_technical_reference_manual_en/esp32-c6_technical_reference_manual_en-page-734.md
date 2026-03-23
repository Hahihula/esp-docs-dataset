

```markdown
| UART Feature | LP_UART Feature |
|--------------|-----------------|
| Special character AT_CMD detection |                 |
| RS485 protocol | —               |
| IrDA protocol | —               |
| High-speed data communication using GDMA | —               |
| Receive timeout |                 |
| UART as wake-up source | Software and hardware flow control |
| Three prescalable clock sources<br>1. APB_CLK<br>2. XTAL_CLK<br>3. RC_FAST_CLK | Two prescalable clock sources<br>1. XTAL_D2_CLK<br>2. LP_FAST_CLK |
```

## 27.3 UART Structure

Figure 27.3-1 shows the basic structure of a UART controller. A UART controller works in four clock domains, namely APB_CLK, AHB_CLK, UART_SCLK, and UART_FCLK. APB_CLK and AHB_CLK are synchronized but with different frequencies (APB_CLK is derived from AHB_CLK by division), and likewise UART_SCLK and UART_FCLK are synchronized but with different frequencies (UART_SCLK is derived from UART_FCLK by division). UART_FCLK has three clock sources: an 80 MHz PLL_F80M_CLK, RC_FAST_CLK, and external
```