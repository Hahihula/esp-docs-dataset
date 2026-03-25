
```markdown
1. Set `EFUSE_BLK_NUM` to the block number.
2. Write into `EFUSE_PGM_DATA0_REG ~ EFUSE_PGM_DATA7_REG` the data to be programmed. Write into `EFUSE_PGM_CHECK_VALUE0_REG ~ EFUSE_PGM_CHECK_VALUE2_REG` the corresponding RS code.

## Programming process

The process of programming parameters is as follows:

1. Configure the value of parameter `EFUSE_BLK_NUM` to determine the block to be programmed.
2. Write parameters to be programmed to registers `EFUSE_PGM_DATA0_REG ~ EFUSE_PGM_DATA7_REG` and `EFUSE_PGM_CHECK_VALUE0_REG ~ EFUSE_PGM_CHECK_VALUE2_REG`.
3. Make sure the eFuse programming voltage VDDQ is configured correctly as described in Section 5.3.4.
4. Configure the field `EFUSE_OP_CODE` of register `EFUSE_CONF_REG` to `0x5A5A`.
5. Configure the field `EFUSE_PGM_CMD` of register `EFUSE_CMD_REG` to 1.
6. Poll register `EFUSE_CMD_REG` until it is `0x0`, or wait for a PGM_DONE interrupt. For more information on how to identify a PGM_DONE or READ_DONE interrupt, please see the end of Section 5.3.3.
7. Clear the parameters in `EFUSE_PGM_DATA0_REG ~ EFUSE_PGM_DATA7_REG` and `EFUSE_PGM_CHECK_VALUE0_REG ~ EFUSE_PGM_CHECK_VALUE2_REG`.
8. Trigger an eFuse read operation (see Section 5.3.3) to update eFuse registers with the new values.
9. Check error record registers. If the values read in error record registers are not 0, the programming process should be performed again following above steps 1 ~ 7. Please check the following error record registers for different eFuse blocks:

    - BLOCK0: `EFUSE_RD_REPEAT_ERR_REG ~ EFUSE_RD_REPEAT_ERR4_REG`
    - BLOCK1: `EFUSE_MAC_SYS_ERR_NUM, EFUSE_MAC_SYS_FAIL`
    - BLOCK2: `EFUSE_SYS_PART1_ERR_NUM, EFUSE_SYS_PART1_FAIL`
    - BLOCK3: `EFUSE_USR_DATA_ERR_NUM, EFUSE_USR_DATA_FAIL`
    - BLOCK4: `EFUSE_KEY0_ERR_NUM, EFUSE_KEY0_FAIL`
    - BLOCK5: `EFUSE_KEY1_ERR_NUM, EFUSE_KEY1_FAIL`
    - BLOCK6: `EFUSE_KEY2_ERR_NUM, EFUSE_KEY2_FAIL`
    - BLOCK7: `EFUSE_KEY3_ERR_NUM, EFUSE_KEY3_FAIL`
    - BLOCK8: `EFUSE_KEY4_ERR_NUM, EFUSE_KEY4_FAIL`
    - BLOCK9: `EFUSE_KEY5_ERR_NUM, EFUSE_KEY5_FAIL`
    - BLOCK10: `EFUSE_SYS_PART2_ERR_NUM, EFUSE_SYS_PART2_FAIL`

## Limitations

In BLOCK0, each bit can be programmed separately. However, we recommend to minimize programming cycles and program all the bits of a parameter in one programming action. In addition, after all parameters controlled by a certain bit of `EFUSE_WR_DIS` are programmed, that bit should be immediately programmed.
```