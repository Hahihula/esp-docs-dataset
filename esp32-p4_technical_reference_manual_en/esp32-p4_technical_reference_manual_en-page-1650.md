

```markdown
Chapter 36 Image Signal Processor (ISP)

GoBack

• CSI_BRIG_DMABLK_SIZE configures the number of VDMA bursts in a VDMA block transfer. If an image frame is transferred with only one block, and this block contains n VDMA bursts, then configure this field to a value greater than n. It is recommended to set it to the maximum value, 0x1FFF.

36.5.8 Color Mode and Byte Order

36.5.8.1 Output Pixel Layout Format

When the ISP is disabled, ISP_Tail directly receives Image Interface 32 data from the MIPI CSI HOST. The pixel layout can be referenced from Chapter 40 MIPI CSI. In this case, the Image Interface 32 data output from CSI HOST can go through two levels of byte ordering in ISP_Tail and CSI_Bridge, refer to Byte Order for details.

After the ISP is enabled and the data has been processed by the ISP_Pipeline, the layout format of the output pixel is as shown in Table 36.5-2.

Table 36.5-2. ISP Output Pixel Layout Format

<table>
<thead>
<tr>
<th>Color Mode</th><th>Addr + 7</th><th>Addr + 6</th><th>Addr + 5</th><th>Addr + 4</th><th>Addr + 3</th><th>Addr + 2</th><th>Addr + 1</th><th>Addr + 0</th>
</tr>
</thead>
<tbody>
<tr>
<td>RAW8</td><td>RAW7[7:0]</td><td>RAW6[7:0]</td><td>RAW5[7:0]</td><td>RAW4[7:0]</td><td>RAW3[7:0]</td><td>RAW2[7:0]</td><td>RAW1[7:0]</td><td>RAWO[7:0]</td>
</tr>
<tr>
<td></td><td>G2[7:0]</td><td>B2[7:0]</td><td>R1[7:0]</td><td>G1[7:0]</td><td>B1[7:0]</td><td>RO[7:0]</td><td>GO[7:0]</td><td>BO[7:0]</td>
</tr>
<tr>
<td>RGB888</td><td>B5[7:0]</td><td>R4[7:0]</td><td>G4[7:0]</td><td>B4[7:0]</td><td>R3[7:0]</td><td>G3[7:0]</td><td>B3[7:0]</td><td>R2[7:0]</td>
</tr>
<tr>
<td></td><td>R7[7:0]</td><td>G7[7:0]</td><td>B7[7:0]</td><td>R6[7:0]</td><td>G6[7:0]</td><td>B6[7:0]</td><td>R5[7:0]</td><td>G5[7:0]</td>
</tr>
<tr>
<td>RGB565</td><td>R3[4:0]G3[5:3]</td><td>G3[2:0]B3[4:0]</td><td>R2[4:0]G2[5:3]</td><td>G2[2:0]B2[4:0]</td><td>R1[4:0]G1[5:3]</td><td>G1[2:0]B1[4:0]</td><td>RO[4:0]GO[5:3]</td><td>GO[2:0]BO[4:0]</td>
</tr>
<tr>
<td>YUV422</td><td>Y3[7:0]</td><td>V2[7:0]</td><td>Y2[7:0]</td><td>U2[7:0]</td><td>Y1[7:0]</td><td>VO[7:0]</td><td>YO[7:0]</td><td>UO[7:0]</td>
</tr>
<tr>
<td>YUV420 (Odd-numbered rows)</td><td>Y4[7:0]</td><td>U4[7:0]</td><td>Y3[7:0]</td><td>Y2[7:0]</td><td>U2[7:0]</td><td>Y1[7:0]</td><td>YO[7:0]</td><td>UO[7:0]</td>
</tr>
<tr>
<td></td><td>U10[0:7]</td><td>Y9[7:0]</td><td>Y8[7:0]</td><td>U8[0:7]</td><td>Y7[7:0]</td><td>Y6[7:0]</td><td>U6[7:0]</td><td>Y5[7:0]</td>
</tr>
<tr>
<td></td><td>Y15[7:0]</td><td>Y14[7:0]</td><td>U14[0:7]</td><td>Y13[7:0]</td><td>Y12[7:0]</td><td>U12[7:0]</td><td>Y11[7:0]</td><td>Y10[7:0]</td>
</tr>
<tr>
<td>YUV420 (Even-numbered rows)</td><td>Y4[7:0]</td><td>V4[7:0]</td><td>Y3[7:0]</td><td>V2[7:0]</td><td>Y2[7:0]</td><td>Y1[7:0]</td><td>YO[7:0]</td><td>VO[7:0]</td>
</tr>
<tr>
<td></td><td>V10[0:7]</td><td>Y9[7:0]</td><td>Y8[7:0]</td><td>V8[0:7]</td><td>Y7[7:0]</td><td>Y6[7:0]</td><td>V6[7:0]</td><td>Y5[7:0]</td>
</tr>
<tr>
<td></td><td>Y15[7:0]</td><td>Y14[7:0]</td><td>V14[0:7]</td><td>Y13[7:0]</td><td>Y12[7:0]</td><td>V12[7:0]</td><td>Y11[7:0]</td><td>Y10[7:0]</td>
</tr>
</tbody>
</table>

36.5.8.2 Byte Order

CSI_Bridge can reorder the bytes of the input 64-bit data via CSI_BRIG_BYTE_ENDIAN_ORDER. ISP_Tail can also reorder the bytes via ISP_BYTE_ENDIAN_ORDER. The byte ordering functionality within ISP_Tail differs from that of CSI_Bridge, as illustrated in Figure 36.5-4.

• ISP_Tail byte ordering: This operation applies to its Image Interface 32 input. It reverses the high and low bytes of the 32-bit input data and then concatenates them to output 64-bit data. This step only functions when the ISP is disabled and is mainly used for processing Image Interface 32 YUV422 and YUV420 input types.

• CSI_Bridge byte ordering: This operation acts on the 64-bit input data (i.e., the output data from ISP_Tail) by reversing its high and low bytes.
```