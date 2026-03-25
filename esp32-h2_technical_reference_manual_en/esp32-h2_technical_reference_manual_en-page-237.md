

```markdown
|26|GPIO26|USB_D-|-|
|:----|:-------|:--------|:-:|
|27|GPIO27|USB_D+| - |
```

1. ZCDO and ZCD1 are analog PAD voltage comparator functions. See subsection 6.15 for details.

## 6.15 Function of Analog PAD Voltage Comparator

GPIO10 and GPIO11 pads have the function of analog PAD voltage comparator, which can be enabled by setting `GPIO_EXT_XPD_COMP` to 1. After enabling the function of analog PAD voltage comparator, when the voltage on GPIO11 pad is higher than the reference voltage, the `PAD_COMP_OUT` signal indicating the comparison result will be high, otherwise it will be low.

Set the value of `GPIO_EXT_MODE_COMP` as follows:

*   0: the reference voltage is `(GPIO_EXT_DREF_COMP * VDDPST2) / 10`.
*   1: the reference voltage is the voltage on GPIO10 PAD.

The `PAD_COMP_OUT` signal will be synchronized to the operating clock of the IO MUX to generate the `PAD_COMP_OUT_sync` signal, which will be used as the interrupt source `GPIO_EXT_PAD_COMP_INT`.

Set the value of `GPIO_EXT_ZERO_DET_MODE` as follows:

*   0: disable interrupt source generation.
*   1, 2: reserved
*   3: enable interrupt source and set any edge of `PAD_COMP_OUT_sync` signal as interrupt source.

Meanwhile, after generating an interrupt source, new interrupt sources will be masked within `GPIO_EXT_ZERO_DET_FILTER_CNT` IO MUX operating clock cycles.

## 6.16 Event Task Matrix Function

In ESP32-H2, GPIO supports ETM function, that is, the ETM task of GPIO can be triggered by the ETM event of any peripheral, or the ETM task of any peripheral can be triggered by the ETM event of GPIO. For more details about ETM, please refer to Chapter 10 Event Task Matrix (SOC_ETM). Only ETM tasks and ETM events related to GPIO are introduced here.

The GPIO ETM provides eight task channels `x` (0 ~ 7). The ETM tasks that each task channel can receive are:

*   `GPIO_TASK_CHx_SET`: GPIO goes high when triggered;
*   `GPIO_TASK_CHx_CLEAR`: GPIO goes low when triggered;
*   `GPIO_TASK_CHx_TOGGLE`: GPIO toggle level when triggered.

Below is an example to configure task channel `x` to control `GPIOy`:

*   Configure `IO_MUX_GPIOy_MCU_SEL` to 1, to select Function 1 listed in Table 6.13-1;
*   Configure `GPIO_ENABLE_REG[y]` to 1;
```