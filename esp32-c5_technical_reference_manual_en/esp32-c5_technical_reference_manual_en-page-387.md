

```markdown
MUX > 8.9 Pin Hold Feature)

## 9.2.4 Functional Description

### 9.2.4.1 HP System Clock

As Figure 9.2-1 shows, CPU_CLK is the master clock for CPU and its frequency can be as high as 240 MHz. Alternatively, CPU can run at lower frequencies, such as at 2 MHz, to achieve lower power consumption.

CPU_CLK shares the same clock sources with AHB_CLK and APB_CLK. Users can select from XTAL_CLK, PLL_240M_CLK, PLL_160M_CLK, or RC_FAST_CLK as the clock source of CPU_CLK by configuring PCR_SOC_CLK_SEL. For details, see Table 9.2-1 and Table 9.2-2. By default, the CPU clock is sourced from XTAL_CLK with a division factor of 1.

**Table 9.2-1. CPU_CLK Clock Source**

| PCR_SOC_CLK_SEL | CPU Clock Source |
|------------------|------------------|
| 0                | XTAL_CLK         |
| 1                | RC_FAST_CLK      |
| 2                | PLL_F160M_CLK    |
| 3                | PLL_F240M_CLK    |

**Table 9.2-2. Frequency of CPU_CLK, AHB_CLK and HP_ROOT_CLK**

| Clock           | Source                  | Frequency     |
|------------------|-------------------------|---------------|
|                  | PLL_F240M_CLK           | 240 MHz       |
| HP_ROOT_CLK      | PLL_F160M_CLK           | 160 MHz       |
|                  | XTAL_CLK                | 48 MHz        |
|                  | RC_FAST_CLK             | 20 MHz        |
| CPU_CLK¹         | HP_ROOT_CLK              | f_HP_ROOT_CLK / (PCR_CPU_DIV_NUM + 1) |
| AHB_CLK²         | HP_ROOT_CLK              | f_HP_ROOT_CLK / (PCR_AHB_DIV_NUM + 1) |

---

¹ CPU_CLK frequency must be larger than or equal to AHB_CLK frequency, and must be an integer multiple of AHB_CLK frequency.

² AHB_CLK frequency can not exceed XTAL_CLK frequency.

**Note:**

When selecting the clock source of HP_ROOT_CLK, or configuring the clock divisor for CPU_CLK and AHB_CLK, please also set `PCR_BUS_CLOCK_UPDATE` to apply the new configuration, and read `PCR_BUS_CLOCK_UPDATE` to see if new configuration takes effect.

As shown in 9.2-1, to generate APB_CLK, AHB_CLK might be divided twice. The first division is compulsory. That is, AHB_CLK is always divided by the divisor (`PCR_APB_DIV_NUM + 1`). The second division (also called automatic frequency reduction) is optional. When there is no request from the host in the chip to access peripheral registers, AHB_CLK will be further divided by (`APB_DECREASE_DIV_NUM + 1`) to lower power consumption. If the host initiates a request to access peripheral registers, APB_CLK will be restored to the frequency after the first division.
```