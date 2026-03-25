

```markdown
Chapter 7 eFuse Controller (EFUSE) GoBack

7.3.2 Programming of Parameters

The eFuse controller can only program eFuse parameters in one block at a time. BLOCK0 ~ BLOCK10 share the same address range to store the parameters to be programmed. Configure parameter EFUSE_BLK_NUM to indicate which block to program.

Each programming register corresponds to a reading register (see Table 7.3-4 for details). To find the data's programming location, refer to the parameter's location in the reading registers.

For example, to program EFUSE_USB_EXCHG_PINS in BLOCK0:

1. Identify its location in the reading data registers, which is the 25th bit in EFUSE_RD_REPEAT_DATA0_REG
2. Set the 25th bit in EFUSE_PGM_DATA1_REG to 1.
3. Follow the steps below to program the bit in eFuse memory.

Programming preparation

- Confirm clock frequency (48 MHz)
- Program BLOCK0

    1. Set EFUSE_BLK_NUM to 0.
    2. Write into EFUSE_PGM_DATA0_REG ~ EFUSE_PGM_DATA5_REG the data to be programmed to BLOCK0.
        The data in EFUSE_PGM_DATA6_REG ~ EFUSE_PGM_DATA7_REG and
        EFUSE_PGM_CHECK_VALUE0_REG ~ EFUSE_PGM_CHECK_VALUE2_REG does not affect the programming of BLOCK0.

- BLOCK1 cannot be programmed by users as it has been programmed at manufacturing.

- Program BLOCK2 ~ 10

    1. Set EFUSE_BLK_NUM to the block number.
    2. Write into EFUSE_PGM_DATA0_REG ~ EFUSE_PGM_DATA7_REG the data to be programmed. Write into EFUSE_PGM_CHECK_VALUE0_REG ~ EFUSE_PGM_CHECK_VALUE2_REG the corresponding RS code.

Programming process

The process of programming parameters is as follows:

1. Configure the value of parameter EFUSE_BLK_NUM to determine the block to be programmed.
2. Write parameters to be programmed to registers EFUSE_PGM_DATA0_REG ~ EFUSE_PGM_DATA7_REG and EFUSE_PGM_CHECK_VALUE0_REG ~ EFUSE_PGM_CHECK_VALUE2_REG.
3. Make sure the eFuse programming voltage VDDQ is configured correctly as described in Section 7.3.4.
4. Configure the field EFUSE_OP_CODE of register EFUSE_CONF_REG to 0x5A5A.
5. Configure the field EFUSE_PGM_CMD of register EFUSE_CMD_REG to 1.
6. Poll register EFUSE_CMD_REG until it is 0x0, or wait for a PGM_DONE interrupt. For more information on how to identify a PGM_DONE or READ_DONE interrupt, please see the end of Section 7.3.3.
```