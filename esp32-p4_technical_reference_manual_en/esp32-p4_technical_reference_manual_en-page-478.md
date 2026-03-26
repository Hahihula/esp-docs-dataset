

```markdown
Chapter 7 System and Memory

HP L2MEM can be accessed by various peripherals:

*   by USB 2.0 High-speed, USB 2.0 Full-speed, GMAC, SDMMC, TRACE, GDMA-AHB, and SYSMON via AHB matrix.
*   by GDMA, GDMA-AXI, 2D-DMA, and H264 Encoder via AXI matrix.

The HP L2MEM supports Error Correction Code (ECC) check to correct one-bit memory flip error. In the event of a one-bit flip error, the data in HP L2MEM still remains valid. Before ECC check, HP L2MEM itself must be initialized first.

HP L2MEM consists of six memory units, each occupying 128 KB. The initialization process allows individual configuration of each unit for power considerations. It is recommended to initialize memory units sequentially rather than simultaneously. This sequential approach helps prevent excessive power consumption and avoids triggering a brownout condition when initializing the entire 768 KB HP L2MEM.

Detailed Configuration Steps:

Take unit0 as an example, other units follow the same configuration steps.

*   Set `HP_SYSTEM_L2_MEM_UNIT0_REFRESH_EN` and clear `HP_SYSTEM_L2_MEM_REFRESH_CNT_RESET` to start initializing HP L2MEM.
*   Read the value of `HP_SYSTEM_L2_MEM_UNIT0_REFRESH_DONE`.
*   Once `HP_SYSTEM_L2_MEM_UNIT0_REFRESH_DONE` reaches a value of 1, set `HP_SYSTEM_L2_RAM_UNIT0_ECC_EN` to start ECC check.
*   (Recommended) clear `HP_SYSTEM_L2_MEM_UNIT0_REFRESH_EN` and set `HP_SYSTEM_L2_MEM_REFRESH_CNT_RESET` after `HP_SYSTEM_L2_MEM_UNIT0_REFRESH_DONE` reaches 1 to complete the initialization process.

During the initialization process, avoid any access to HP L2MEM unit being initialized.

3. Details for LP ROM

This 16 KB LP ROM is a read-only memory accessed by LP CPU through the instruction bus or data bus via their shared address `0x5010_0000 ~ 0x5010_3FFF` as shown in Table 7.3-1.

4. Details for LP SRAM

This 32 KB LP SRAM is a read-and-write memory accessed by the HP CPU via AHB matrix and by the LP CPU through the instruction bus or data bus via their shared address `0x5010_8000 ~ 0x5010_FFFF` as shown in Table 7.3-1. LP SRAM supports atomic operation.

5. Details for HP SPM

This 8 KB HP SPM is a read-and-write memory accessed by the HP CPU through the instruction bus or data bus via their shared address `0x3010_0000 ~ 0x3010_1FFF` as shown in Table 7.3-1. Additionally, HP SPM supports atomic operation of the HP CPU.

HP SPM supports parity check to detect one-bit memory flip error. Before conducting the parity check, HP SPM itself must be initialized first.

Detailed Configuration Steps:

*   Set `HP_SYSTEM_SPM_INIT_EN` and clear `HP_SYSTEM_SPM_INIT_CNT_RESET` to start initializing HP SPM.
```