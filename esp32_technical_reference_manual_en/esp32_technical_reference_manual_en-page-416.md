**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Body Text:**
well as receiving and transmitting PDM signals.

The right side of Figure **22.1-1** shows the signal bus of the I2S module. The signal naming rule of the Rx and Tx units is `I2SnA_B_C`, where `"n"` stands for either I2S0 or I2S1; "A" represents the direction of I2S module's data bus signal, "l" represents input, "O" represents output; "B" represents signal function; "C" represents the signal direction, "in" means that the signal is input into the I2S module, while "out" means that the I2S module outputs the signal. For a detailed description of the I2S signal bus, please refer to Table **22.1-1**. Table 22.1-1 describes the signal bus of the I2S MUX. Except for the `I2Sn_CLK` signal, all other signals are mapped to the chip pin via the GPIO matrix and IO MUX. The `I2Sn_CLK` signal is mapped to the chip pin via the IO_MUX.

For details, please refer to the chapter about **IO_MUX** and the GPIO Matrix.

**Table Title:**
Table 22.1-1. I2S Signal Bus Description

| Signal Bus | Signal Direction | Data Signal Direction |
|------------|------------------|-----------------------|
| `I2Sn_BCK_in` | In slave mode, I2S module inputs signals. | I2S module receives data. |
| `I2Sn_BCK_out` | In master mode, I2S module outputs signals. | I2S module receives data. |
| `I2Sn_WS_in` | In slave mode, I2S module inputs signals. | I2S module receives data. |
| `I2Sn_WS_out` | In master mode, I2S module outputs signals. | I2S module receives data. |
| `I2Sn_Data_in1` | I2S module inputs signals. | In I2S mode, `I2Sn_Data_in[15]` is the serial data bus of I2S. In LCD mode, the data bus width can be configured as needed. |
| `I2Sn_O_Data_out1` | I2S module outputs signals. | In I2S mode, `I2SnO_Data_out[23]` is the serial data bus of I2S. In LCD mode, the data bus width can be configured as needed. |
| `I2Sn_BCK_in` | In slave mode, I2S module inputs signals. | I2S module sends data. |
| `I2Sn_BCK_out` | In master mode, I2S module outputs signals. | I2S module sends data. |
| `I2Sn_WS_in` | In slave mode, I2S module inputs signals. | I2S module sends data. |
| `I2Sn_WS_out` | In master mode, I2S module outputs signals. | I2S module sends data. |
| `I2Sn_CLK2` | I2S module outputs signals. | It is used as a clock source for peripheral chips. |
| `I2Sn_H_SYNC` |  | The signals are sent from the Camera. |
| `I2Sn_V_SYNC` | In camera mode, I2S module inputs signals. |  |
| `I2SnH_ENABLE` |  |  |

**Note:**
1. Assume that the bit width of the input/output signal is `"N"`, the input signal should be configured to `I2Sn_Data_in[0]`, and the output signal to `I2SnO_Data_out[23:`-`N+1]`. Generally, for input signals, `"N"`=8 or 16; while for output signals, `"N"`=8, 16 or 24 (note that I2S1 does not support 24-bit width).
2. `I2Sn_CLK` can only be mapped to GPIO0, UORXD (GPIO3) or UOTXD (GPIO1) by selecting GPIO functions CLK_OUT1, CLK_OUT2, or CLK_OUT3. For more information, see Table **6.10-1**: IO_MUX Pin Summary.

**Footer:**
Espressif Systems
416 ESP32 TRM (Version 5.6)
Submit Documentation Feedback