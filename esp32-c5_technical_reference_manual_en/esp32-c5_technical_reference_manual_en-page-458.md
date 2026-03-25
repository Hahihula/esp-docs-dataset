

```markdown
## Register 9.90. LP_CLKRST_RESET_CAUSE_REG (0x0010)

LP_CLKRST_COREO_RESET_FLAG_CLR  
LP_CLKRST_COREO_RESET_FLAG_SET  
LP_CLKRST_COREO_RESET_CAUSE_CLR  

(reserved)  

| 31 | 30 | 29 | ... | 6 | 5 | 4 | ... | Reset |
|----:|----:|----:|-----:|---:|---:|---:|-----:|-------|
|   0 |   0 |   0 | 0    |   0 |   1 |   0 |       |       |

LP_CLKRST_RESET_CAUSE Represents the reset cause. (RO)

LP_CLKRST_COREO_RESET_FLAG Represents whether the reset occurred is recorded in LP_CLKRST_RESET_CAUSE.

- 0: Illegal reset
- 1: Recorded reset

(RO)

LP_CLKRST_COREO_RESET_CAUSE_CLR Write 1 to clear LP_CLKRST_RESET_CAUSE. (WT)

LP_CLKRST_COREO_RESET_FLAG_SET Write 1 to set LP_CLKRST_COREO_RESET_FLAG. (WT)

LP_CLKRST_COREO_RESET_FLAG_CLR Write 1 to clear LP_CLKRST_COREO_RESET_FLAG. (WT)
```