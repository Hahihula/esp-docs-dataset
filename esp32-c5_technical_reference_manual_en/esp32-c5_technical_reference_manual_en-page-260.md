

```markdown
7. Clear the parameters in EFUSE_PGM_DATAO_REG ~ EFUSE_PGM_DATA7_REG and  
   EFUSE_PGM_CHECK_VALUE0_REG ~ EFUSE_PGM_CHECK_VALUE2_REG.

8. Trigger an eFuse read operation (see Section 7.3.3) to update eFuse registers with the new values.

9. Check error record registers. If the values read in error record registers are not 0, the programming  
   process should be performed again following above steps 1 ~ 7. Please check the following error record  
   registers for different eFuse blocks:

* BLOCK0: EFUSE_RD_REPEAT_DATA_ERR_REG ~ EFUSE_RD_REPEAT_DATA_ERR4_REG
* BLOCK1: EFUSE_RD_MAC_SYS_ERR_NUM, EFUSE_RD_MAC_SYS_FAIL
* BLOCK2: EFUSE_RD_SYS_PART1_DATA_ERR_NUM, EFUSE_RD_SYS_PART1_DATA_FAIL
* BLOCK3: EFUSE_RD_USR_DATA_ERR_NUM, EFUSE_RD_USR_DATA_FAIL
* BLOCK4: EFUSE_RD_KEY0_DATA_ERR_NUM, EFUSE_RD_KEY0_DATA_FAIL
* BLOCK5: EFUSE_RD_KEY1_DATA_ERR_NUM, EFUSE_RD_KEY1_DATA_FAIL
* BLOCK6: EFUSE_RD_KEY2_DATA_ERR_NUM, EFUSE_RD_KEY2_DATA_FAIL
* BLOCK7: EFUSE_RD_KEY3_DATA_ERR_NUM, EFUSE_RD_KEY3_DATA_FAIL
* BLOCK8: EFUSE_RD_KEY4_DATA_ERR_NUM, EFUSE_RD_KEY4_DATA_FAIL
* BLOCK9: EFUSE_RD_KEY5_DATA_ERR_NUM, EFUSE_RD_KEY5_DATA_FAIL
* BLOCK10: EFUSE_RD_SYS_PART2_DATA_ERR_NUM, EFUSE_RD_SYS_PART2_DATA_FAIL

Limitations

In BLOCK0, each bit can be programmed separately. However, we recommend to minimize programming  
cycles and program all the bits of a parameter in one programming action. In addition, after all parameters  
controlled by a certain bit of EFUSE_WR_DIS are programmed, that bit should be immediately programmed.  
The programming of parameters controlled by a certain bit of EFUSE_WR_DIS, and the programming of the bit  
itself can even be completed at the same time in one programming action.

BLOCK1 cannot be programmed by users as it has been programmed at manufacturing.

BLOCK2 ~ 10 can only be programmed once. Repeated programming is not allowed.
```

```markdown
## 7.3.3 Reading of Parameters

Users cannot read eFuse bits directly. The eFuse controller hardware reads all eFuse bits and stores the  
results to their corresponding registers in its memory space. Then, users can read eFuse bits by reading the  
registers that start with EFUSE_RD_. Details are provided in Table 7.3-4.

Table 7.3-4. Registers Information

| BLOCK | Read Registers                          | Registers When Programming This Block |
|-------|------------------------------------------|----------------------------------------|
| 0     | EFUSE_RD_WR_DIS_REG                     | EFUSE_PGM_DATAO_REG                   |
|       | EFUSE_RD_REPEAT_DATAn_REG (n: 0 ~ 4)    | EFUSE_PGM_DATAn_REG (n: 1 ~ 5)        |
| 1     | EFUSE_RD_MAC_SYS_n_REG (n: 0 ~ 5)       | EFUSE_PGM_DATAn_REG (n: 0 ~ 5)        |
| 2     | EFUSE_RD_SYS_PART1_DATAn_REG (n: 0 ~ 7) | EFUSE_PGM_DATAn_REG (n: 0 ~ 7)        |

Cont'd on next page
```