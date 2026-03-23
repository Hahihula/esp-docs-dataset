

```markdown
Chapter 34 On-Chip Sensor and Analog Signal Processing

GoBack

* Channel O of SAR ADC2, with the attenuation of 2.5 dB

The detailed configuration is as follows:

* Configure the first pattern table entry (cmd0):

![Figure 34.2-6. cmd0 Configuration](image)

<table>
<thead>
<tr>
<th></th>
<th>5</th>
<th>4</th>
<th>2</th>
<th>1</th>
<th>0</th>
</tr>
</thead>
<tbody>
<tr>
<td>sar_sel</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>ch_sel</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>atten</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>0</td>
<td>2</td>
<td></td>
<td>3</td>
<td></td>
</tr>
</tbody>
</table>

atten write the value of 3 to this field, to set the attenuation to 12 dB.

ch_sel write the value of 2 to this field, to select channel 2 (see Table 34.2-1).

sar_sel write the value of O to this bit, to select SAR ADC1 as the working ADC.

* Configure the second pattern table entry (cmd1):

![Figure 34.2-7. cmd1 configuration](image)

<table>
<thead>
<tr>
<th></th>
<th>5</th>
<th>4</th>
<th>2</th>
<th>1</th>
<th>0</th>
</tr>
</thead>
<tbody>
<tr>
<td>sar_sel</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>ch_sel</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>atten</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td>1</td>
<td>0</td>
<td></td>
<td>1</td>
<td></td>
</tr>
</tbody>
</table>

atten write the value of 1 to this field, to set the attenuation to 2.5 dB.

ch_sel write the value of O to this field, to select channel O (see Table 34.2-1).

sar_sel write the value of 1 to this bit, to select SAR ADC2 as the working ADC.

* Configure APB_SARADC_SAR_PATT_LEN to 1, i.e., set pattern table length to (this value + 1 = 2). Then pattern table entries cmd0 and cmd1 will be used.
* Enable the timer, then DIG ADC controller starts scanning the two channels in cycles, as configured in the pattern table entries.

DMA Data Format

The ADC eventually passes 32-bit data to the DMA, see the figure below.

![Figure 34.2-8. DMA Data Format](image)

data SAR ADC read value, 12-bit
ch_sel Channel, 3-bit
sar_sel SAR ADC selection, 1-bit
```