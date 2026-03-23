

```markdown
| BLOCK | Parameters                  | Bit Width | Accessible by Hardware | Write Protection by EFUSE_WR_DIS Bit Number | Read Protection by EFUSE_RD_DIS Bit Number | Description          |
|-------|-----------------------------|-----------|------------------------|----------------------------------------------|---------------------------------------------|----------------------|
| BLOCK1|                             |           |                        |                                              |                                             |                      |
|       | EFUSE_MAC                   | 48        | N                      | 20                                           | N/A                                          | MAC address          |
|       | EFUSE_MAC_EXT               | 16        | N                      | 20                                           | N/A                                          | Extended MAC address |
|       | EFUSE_SYS_DATA_PARTO        | 69        | N                      | 20                                           | N/A                                          | System data          |
| BLOCK2| EFUSE_SYS_DATA_PART1       | 256       | N                      | 21                                           | N/A                                          | System data          |
| BLOCK3| EFUSE_USR_DATA              | 256       | N                      | 22                                           | N/A                                          | User data            |
| BLOCK4| EFUSE_KEYO_DATA             | 256       | Y                      | 23                                           | 0                                            | KEY0 or user data    |
| BLOCK5| EFUSE_KEY1_DATA             | 256       | Y                      | 24                                           | 1                                            | KEY1 or user data    |
| BLOCK6| EFUSE_KEY2_DATA             | 256       | Y                      | 25                                           | 2                                            | KEY2 or user data    |
| BLOCK7| EFUSE_KEY3_DATA             | 256       | Y                      | 26                                           | 3                                            | KEY3 or user data    |
| BLOCK8| EFUSE_KEY4_DATA             | 256       | Y                      | 27                                           | 4                                            | KEY4 or user data    |
| BLOCK9| EFUSE_KEY5_DATA             | 256       | Y                      | 28                                           | 5                                            | KEY5 or user data    |
| BLOCK10| EFUSE_SYS_DATA_PART2      | 256       | N                      | 29                                           | 6                                            | System data          |
```