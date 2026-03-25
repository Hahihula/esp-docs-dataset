

```markdown
- Receive timeout
- UART as wake-up source
- Software and hardware flow control
- Three prescalable clock sources: PLL_F48M_CLK, XTAL_CLK, and RC_FAST_CLK

## 28.3 UART Structure

Figure 28.3-1 shows the basic structure of a UART controller. A UART controller works in four clock domains, namely APB_CLK, AHB_CLK, UART_SCLK, and UART_FCLK. APB_CLK and AHB_CLK are synchronized but with different frequencies (APB_CLK is derived from AHB_CLK by division), and likewise UART_SCLK and UART_FCLK are synchronized but with different frequencies (UART_SCLK is derived from UART_FCLK by division). UART_FCLK has three clock sources: 48 MHz PLL_F48M_CLK, RC_FAST_CLK, and external crystal clock XTAL_CLK (for details, please refer to Chapter 7 Reset and Clock), which are selected by configuring PCR_UARTn_SCLK_SEL. The selected clock source is divided by a divider to generate UART_SCLK clock signals. The divisor is configured by PCR_UARTn_SCLK_DIV_NUM for the integral part, PCR_UARTn_SCLK_DIV_A for the denominator of the fractional part, and PCR_UARTn_SCLK_DIV_B for the numerator of the fractional part. The divisor ranges from 1 ~ 256.
```