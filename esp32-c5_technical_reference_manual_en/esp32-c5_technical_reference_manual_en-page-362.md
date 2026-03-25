

```markdown
Register 8.34. GPIO_EXT_ETM_TASK_P1_CFG_REG (0x015C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0x0| (reserved) | GPIO_EXT_ETM_TASK_GPIO5_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO6_EN | GPIO_EXT_ETM_TASK_GPIO7_EN | GPIO_EXT_ETM_TASK_GPIO8_SEL | GPIO_EXT_ETM_TASK_GPIO9_SEL | GPIO_EXT_ETM_TASK_GPIO10_SEL | GPIO_EXT_ETM_TASK_GPIO11_SEL | GPIO_EXT_ETM_TASK_GPIO12_SEL | GPIO_EXT_ETM_TASK_GPIO13_SEL | GPIO_EXT_ETM_TASK_GPIO14_SEL | GPIO_EXT_ETM_TASK_GPIO15_SEL | GPIO_EXT_ETM_TASK_GPIO16_SEL | GPIO_EXT_ETM_TASK_GPIO17_SEL | GPIO_EXT_ETM_TASK_GPIO18_SEL | GPIO_EXT_ETM_TASK_GPIO19_SEL | GPIO_EXT_ETM_TASK_GPIO20_SEL | GPIO_EXT_ETM_TASK_GPIO21_SEL | GPIO_EXT_ETM_TASK_GPIO22_SEL | GPIO_EXT_ETM_TASK_GPIO23_SEL | GPIO_EXT_ETM_TASK_GPIO24_SEL | GPIO_EXT_ETM_TASK_GPIO25_SEL | GPIO_EXT_ETM_TASK_GPIO26_SEL | GPIO_EXT_ETM_TASK_GPIO27_SEL | GPIO_EXT_ETM_TASK_GPIO28_SEL | GPIO_EXT_ETM_TASK_GPIO29_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO30_SEL | GPIO_EXT_ETM_TASK_GPIO31_SEL | GPIO_EXT_ETM_TASK_GPIO32_SEL | GPIO_EXT_ETM_TASK_GPIO33_SEL | GPIO_EXT_ETM_TASK_GPIO34_SEL | GPIO_EXT_ETM_TASK_GPIO35_SEL | GPIO_EXT_ETM_TASK_GPIO36_SEL | GPIO_EXT_ETM_TASK_GPIO37_SEL | GPIO_EXT_ETM_TASK_GPIO38_SEL | GPIO_EXT_ETM_TASK_GPIO39_SEL | GPIO_EXT_ETM_TASK_GPIO40_SEL | GPIO_EXT_ETM_TASK_GPIO41_SEL | GPIO_EXT_ETM_TASK_GPIO42_SEL | GPIO_EXT_ETM_TASK_GPIO43_SEL | GPIO_EXT_ETM_TASK_GPIO44_SEL | GPIO_EXT_ETM_TASK_GPIO45_SEL | GPIO_EXT_ETM_TASK_GPIO46_SEL | GPIO_EXT_ETM_TASK_GPIO47_SEL | GPIO_EXT_ETM_TASK_GPIO48_SEL | GPIO_EXT_ETM_TASK_GPIO49_SEL | GPIO_EXT_ETM_TASK_GPIO50_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO51_SEL | GPIO_EXT_ETM_TASK_GPIO52_SEL | GPIO_EXT_ETM_TASK_GPIO53_SEL | GPIO_EXT_ETM_TASK_GPIO54_SEL | GPIO_EXT_ETM_TASK_GPIO55_SEL | GPIO_EXT_ETM_TASK_GPIO56_SEL | GPIO_EXT_ETM_TASK_GPIO57_SEL | GPIO_EXT_ETM_TASK_GPIO58_SEL | GPIO_EXT_ETM_TASK_GPIO59_SEL | GPIO_EXT_ETM_TASK_GPIO60_SEL | GPIO_EXT_ETM_TASK_GPIO61_SEL | GPIO_EXT_ETM_TASK_GPIO62_SEL | GPIO_EXT_ETM_TASK_GPIO63_SEL | GPIO_EXT_ETM_TASK_GPIO64_SEL | GPIO_EXT_ETM_TASK_GPIO65_SEL | GPIO_EXT_ETM_TASK_GPIO66_SEL | GPIO_EXT_ETM_TASK_GPIO67_SEL | GPIO_EXT_ETM_TASK_GPIO68_SEL | GPIO_EXT_ETM_TASK_GPIO69_SEL | GPIO_EXT_ETM_TASK_GPIO70_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO71_SEL | GPIO_EXT_ETM_TASK_GPIO72_SEL | GPIO_EXT_ETM_TASK_GPIO73_SEL | GPIO_EXT_ETM_TASK_GPIO74_SEL | GPIO_EXT_ETM_TASK_GPIO75_SEL | GPIO_EXT_ETM_TASK_GPIO76_SEL | GPIO_EXT_ETM_TASK_GPIO77_SEL | GPIO_EXT_ETM_TASK_GPIO78_SEL | GPIO_EXT_ETM_TASK_GPIO79_SEL | GPIO_EXT_ETM_TASK_GPIO80_SEL | GPIO_EXT_ETM_TASK_GPIO81_SEL | GPIO_EXT_ETM_TASK_GPIO82_SEL | GPIO_EXT_ETM_TASK_GPIO83_SEL | GPIO_EXT_ETM_TASK_GPIO84_SEL | GPIO_EXT_ETM_TASK_GPIO85_SEL | GPIO_EXT_ETM_TASK_GPIO86_SEL | GPIO_EXT_ETM_TASK_GPIO87_SEL | GPIO_EXT_ETM_TASK_GPIO88_SEL | GPIO_EXT_ETM_TASK_GPIO89_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO90_SEL | GPIO_EXT_ETM_TASK_GPIO91_SEL | GPIO_EXT_ETM_TASK_GPIO92_SEL | GPIO_EXT_ETM_TASK_GPIO93_SEL | GPIO_EXT_ETM_TASK_GPIO94_SEL | GPIO_EXT_ETM_TASK_GPIO95_SEL | GPIO_EXT_ETM_TASK_GPIO96_SEL | GPIO_EXT_ETM_TASK_GPIO97_SEL | GPIO_EXT_ETM_TASK_GPIO98_SEL | GPIO_EXT_ETM_TASK_GPIO99_SEL | GPIO_EXT_ETM_TASK_GPIO100_SEL | GPIO_EXT_ETM_TASK_GPIO101_SEL | GPIO_EXT_ETM_TASK_GPIO102_SEL | GPIO_EXT_ETM_TASK_GPIO103_SEL | GPIO_EXT_ETM_TASK_GPIO104_SEL | GPIO_EXT_ETM_TASK_GPIO105_SEL | GPIO_EXT_ETM_TASK_GPIO106_SEL | GPIO_EXT_ETM_TASK_GPIO107_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO108_SEL | GPIO_EXT_ETM_TASK_GPIO109_SEL | GPIO_EXT_ETM_TASK_GPIO110_SEL | GPIO_EXT_ETM_TASK_GPIO111_SEL | GPIO_EXT_ETM_TASK_GPIO112_SEL | GPIO_EXT_ETM_TASK_GPIO113_SEL | GPIO_EXT_ETM_TASK_GPIO114_SEL | GPIO_EXT_ETM_TASK_GPIO115_SEL | GPIO_EXT_ETM_TASK_GPIO116_SEL | GPIO_EXT_ETM_TASK_GPIO117_SEL | GPIO_EXT_ETM_TASK_GPIO118_SEL | GPIO_EXT_ETM_TASK_GPIO119_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO120_SEL | GPIO_EXT_ETM_TASK_GPIO121_SEL | GPIO_EXT_ETM_TASK_GPIO122_SEL | GPIO_EXT_ETM_TASK_GPIO123_SEL | GPIO_EXT_ETM_TASK_GPIO124_SEL | GPIO_EXT_ETM_TASK_GPIO125_SEL | GPIO_EXT_ETM_TASK_GPIO126_SEL | GPIO_EXT_ETM_TASK_GPIO127_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO128_SEL | GPIO_EXT_ETM_TASK_GPIO129_SEL | GPIO_EXT_ETM_TASK_GPIO130_SEL | GPIO_EXT_ETM_TASK_GPIO131_SEL | GPIO_EXT_ETM_TASK_GPIO132_SEL | GPIO_EXT_ETM_TASK_GPIO133_SEL | GPIO_EXT_ETM_TASK_GPIO134_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO135_SEL | GPIO_EXT_ETM_TASK_GPIO136_SEL | GPIO_EXT_ETM_TASK_GPIO137_SEL | GPIO_EXT_ETM_TASK_GPIO138_SEL | GPIO_EXT_ETM_TASK_GPIO139_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO140_SEL | GPIO_EXT_ETM_TASK_GPIO141_SEL | GPIO_EXT_ETM_TASK_GPIO142_SEL | GPIO_EXT_ETM_TASK_GPIO143_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO144_SEL | GPIO_EXT_ETM_TASK_GPIO145_SEL | GPIO_EXT_ETM_TASK_GPIO146_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO147_SEL | GPIO_EXT_ETM_TASK_GPIO148_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO149_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO150_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO151_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO152_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO153_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO154_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO155_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO156_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO157_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO158_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO159_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO160_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO161_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO162_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO163_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO164_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO165_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO166_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO167_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO168_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO169_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO170_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO171_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO172_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO173_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO174_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO175_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO176_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO177_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO178_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO179_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO180_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO181_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO182_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO183_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO184_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO185_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO186_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO187_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO188_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO189_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO190_SEL |
|     |    |    |    |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO191_SEL |
|     |    |    |    |    |    |    |