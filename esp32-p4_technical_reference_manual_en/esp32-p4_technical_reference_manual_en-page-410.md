

```markdown
Table 6.4-7 – cont’d from previous page

| Conversion        | input_sel | proc_en | output_sel | param_sel | param_h0   | param_h1   | param_m0    | param_m1     | param_I0 | param_I1 |
|-------------------|-----------|---------|------------|-----------|------------|------------|-------------|--------------|----------|----------|
| YUV422 → (709)    | 0         | 1       | 1/0        | 12A       | C21E5CB    | 1F252A     | 1338778     | 8752A        | B7D0800  |          |
| RGB888/RGB565     |           |         |            |           |            |            |             |              |          |          |
| YUV444 → (709)    | 2         | 1       | 1/0        | 12A       | C21E5CB    | 1F252A     | 1338778     | 8752A        | B7D0800  |          |
| RGB888/RGB565     |           |         |            |           |            |            |             |              |          |          |

Table 6.4-8. RGB888 Storage Format

| LINE | B1 | G1 | R1 | B2 | G2 | R2 | B3 | G3 | R3 |
|------|----|----|----|----|----|----|----|----|----|
| LSB  |    |    |    |    |    |    | MSB |

Table 6.4-9. YUV444 Storage Format

| LINE | V1 | U1 | Y1 | V2 | U2 | Y2 | V3 | U3 | Y3 |
|------|----|----|----|----|----|----|----|----|----|
| LSB  |    |    |    |    |    |    | MSB |

Table 6.4-10. YUV422 Storage Format

| LINE | U1 | Y1 | V1 | Y2 | U2 | Y3 | V3 | Y4 |
|------|----|----|----|----|----|----|----|----|
| LSB  |    |    |    |    |    | MSB |
```