

```markdown
| Data-Fetching Control Option | Mode | I2S_TX_MONO | I2S_TX_MONO_FST_VLD |
|---|---|---|---|
| Post data-fetching request to DMA at any edge of WS signal | Stereo mode | 0 | x |
| Post data-fetching request to DMA only at the second half period of WS signal | Mono mode | 1 | 0 |
| Post data-fetching request to DMA only at the first half period of WS signal | Mono mode | 1 | 1 |

Table 30.9-5. I2S Channel Control in Normal PDM TX Mode

<table><thead><tr><th>Channel Con-<br/>trol Option</th><th>Left Channel</th><th>Right Channel</th><th>Mode<br/>Control<br/>Field¹</th><th>Channel<br/>Select<br/>Bit²</th></tr></thead><tbody><tr><td rowspan="2">Stereo mode</td><td>Transmit the left channel data</td><td>Transmit the right channel data</td><td>0</td><td>x</td></tr><tr><td>Transmit the left channel data</td><td>Transmit the left channel data</td><td>1</td><td>0</td></tr><tr><td rowspan="6">Mono mode</td><td>Transmit the right channel data</td><td>Transmit the right channel data</td><td>1</td><td>1</td></tr><tr><td>Transmit the left channel data</td><td>Transmit the right channel data</td><td>2</td><td>0</td></tr><tr><td>Transmit the left channel data</td><td>Transmit the left channel data</td><td>2</td><td>1</td></tr><tr><td>Transmit the value of "single"³</td><td>Transmit the right channel data</td><td>3</td><td>0</td></tr><tr><td>Transmit the left channel data</td><td>Transmit the value of "single"</td><td>3</td><td>1</td></tr><tr><td>Transmit the left channel data</td><td>Transmit the value of "single"</td><td>4</td><td>0</td></tr><tr><td></td><td>Transmit the value of "single"</td><td>Transmit the right channel data</td><td>4</td><td>1</td></tr></tbody></table>

¹ I2S_TX_CHAN_MOD
² I2S_TX_WS_IDLE_POL
³ The "single" value is equal to the value of I2S_SINGLE_DATA.

Table 30.9-6. PCM-to-PDM TX Mode

<table><thead><tr><th>Channel Output Format</th><th>I2S_TX_PDM_DAC_MODE_EN</th><th>I2S_TX_PDM_DAC_2OUT_EN</th></tr></thead><tbody><tr><td>1-line PDM output format¹</td><td>0</td><td>x</td></tr><tr><td>1-line DAC output format²</td><td>1</td><td>0</td></tr><tr><td>2-line DAC output format</td><td>1</td><td>1</td></tr></tbody></table>
```