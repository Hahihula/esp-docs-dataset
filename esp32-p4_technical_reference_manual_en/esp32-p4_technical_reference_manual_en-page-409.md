

```markdown
| Conversion | input_sel | proc_en | output_sel | param_h0   | param_h1    | param_m0     | param_m1      | param_IO  | param_I1 |
|------------|-----------|---------|----------|------------|-------------|--------------|---------------|-----------|----------|
| RGB888 → RGB565 | 3         | 0       | 0        | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| RGB565 → RGB888 | 0         | 0       | 2        | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| RGB888 → (601) YUV444 | 3         | 1       | 2        | 20442      | 400019      | 1EDBDA       | 2000070       | 1E8870    | 20003EE  |
| RGB888 → (709) YUV444 | 3         | 1       | 2        | 2742F      | 400010      | 1EABE6       | 2000070       | 1E6870    | 20003F6  |
| RGB888 → (601) YUV422-MIPI | 3         | 1       | 1        | 20442      | 400019      | 1EDBDA       | 2000070       | 1E8870    | 20003EE  |
| RGB888 → (709) YUV422-MIPI | 3         | 1       | 1        | 2742F      | 400010      | 1EABE6       | 2000070       | 1E6870    | 20003F6  |
| YUV444 → (601) RGB888 | 3         | 1       | 2        | 12A        | C86D999     | 1E712A       | 21E4F30       | 8112A     | BAD3000  |
| YUV444 → (709) RGB888 | 3         | 1       | 2        | 12A        | C21E5CB     | 1F252A       | 1338778       | 8752A     | B7D0800  |
| YUV422-MIPI → (601) RGB888 | 1         | 1       | 2        | 12A        | C86D999     | 1E712A       | 21E4F30       | 8112A     | BAD3000  |
| YUV422-MIPI → (709) RGB888 | 1         | 1       | 2        | 12A        | C21E5CB     | 1F252A       | 1338778       | 8752A     | B7D0800  |
```

Table 6.4-7. Parameter Configuration for Color Space Conversion in RX Direction

```markdown
| Conversion                  | input_sel | proc_en | output_sel | param_h0   | param_h1    | param_m0     | param_m1      | param_IO  | param_I1 |
|-----------------------------|-----------|---------|----------|------------|-------------|--------------|---------------|-----------|----------|
| No conversion               | 7         | N/A     | N/A      | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| Only scramble order         | 1/2       | 0       | 1        | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| YUV422 → YUV444              | 0         | 0       | 1        | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| YUV420 → YUV444              | 0         | 0       | 1        | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| YUV444 → YUV422              | 0         | 0       | 2        | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| YUV444 → YUV420              | 0         | 0       | 3        | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| YUV422 → YUV420              | 0         | 0       | 3        | N/A        | N/A         | N/A          | N/A           | N/A       | N/A      |
| YUV420 → (601) RGB888/RGB565| 0         | 1       | 1/0      | 12A        | C86D999     | 1E712A       | 21E4F30       | 8112A     | BAD3000  |
| YUV422 → (601) RGB888/RGB565| 0         | 1       | 1/0      | 12A        | C86D999     | 1E712A       | 21E4F30       | 8112A     | BAD3000  |
| YUV444 → (601) RGB888/RGB565| 2         | 1       | 1/0      | 12A        | C86D999     | 1E712A       | 21E4F30       | 8112A     | BAD3000  |
| YUV420 → (709) RGB888/RGB565| 0         | 1       | 1/0      | 12A        | C21E5CB     | 1F252A       | 1338778       | 8752A     | B7D0800  |
```

Cont'd on next page
```