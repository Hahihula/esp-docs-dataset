
```markdown
| BLOCK | Parameters                     | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Read Protection byEFUSE_RD_DIS Bit Number | Description       |
|-------|---------------------------------|-----------|-------------------------|---------------------------------------------|--------------------------------------------|--------------------|
| BLOCK1| EFUSE_MAC                       | 48        | N                       | 20                                          | N/A                                        | MAC address       |
|       | EFUSE_SPI_PAD_CONFIGURE        |           |                         |                                             |                                            |                    |
|       |                                 | [0:5]     | N                       | 20                                          | N/A                                        | CLK                |
|       |                                 | [6:11]    | N                       | 20                                          | N/A                                        | Q (D1)             |
|       |                                 | [12:17]   | N                       | 20                                          | N/A                                        | D (DO)             |
|       |                                 | [18:23]   | N                       | 20                                          | N/A                                        | CS                 |
|       |                                 | [24:29]   | N                       | 20                                          | N/A                                        | HD (D3)            |
|       |                                 | [30:35]   | N                       | 20                                          | N/A                                        | WP (D2)            |
|       |                                 | [36:41]   | N                       | 20                                          | N/A                                        | DQS                |
|       |                                 | [42:47]   | N                       | 20                                          | N/A                                        | D4                 |
|       |                                 | [48:53]   | N                       | 20                                          | N/A                                        | D5                 |
|       |                                 | [54:59]   | N                       | 20                                          | N/A                                        | D6                 |
|       |                                 | [60:65]   | N                       | 20                                          | N/A                                        | D7                 |
|       | EFUSE_SYS_DATA_PARTO           | 78        | N                       | 20                                          | N/A                                        | System data        |
| BLOCK2| EFUSE_SYS_DATA_PART1           | 256       | N                       | 21                                          | N/A                                        | System data        |
| BLOCK3| EFUSE_USR_DATA                 | 256       | N                       | 22                                          | N/A                                        | User data          |
| BLOCK4| EFUSE_KEYO_DATA                | 256       | Y                       | 23                                          | 0                                          | KEYO or user data  |
| BLOCK5| EFUSE_KEY1_DATA                | 256       | Y                       | 24                                          | 1                                          | KEY1 or user data  |
| BLOCK6| EFUSE_KEY2_DATA                | 256       | Y                       | 25                                          | 2                                          | KEY2 or user data  |
| BLOCK7| EFUSE_KEY3_DATA                | 256       | Y                       | 26                                          | 3                                          | KEY3 or user data  |
| BLOCK8| EFUSE_KEY4_DATA                | 256       | Y                       | 27                                          | 4                                          | KEY4 or user data  |
| BLOCK9| EFUSE_KEY5_DATA                | 256       | Y                       | 28                                          | 5                                          | KEY5 or user data  |
| BLOCK10| EFUSE_SYS_DATA_PART2         | 256       | N                       | 29                                          | 6                                          | System data        |
```