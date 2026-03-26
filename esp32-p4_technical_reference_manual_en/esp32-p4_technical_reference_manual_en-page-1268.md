

```markdown
| Bit | Field Name                                                                 | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                  | -                                                                                                                                           |
| 4   | HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT                                        | Configures whether or not to enable Manual Encryption in SPI Boot mode.                                                                   |
|     |                                                                             | 0: Disable                                                                         |
|     |                                                                             | 1: Enable                                                                          |
|     | (R/W)                                                                        | -                                                                                                                                           |
| 3   | HP_SYSTEM_ENABLE_DOWNLOAD_DB_ENCRYPT                                       | Configures whether or not to enable Auto Encryption in Joint Download Boot mode.                                                         |
|     |                                                                             | 0: Disable                                                                         |
|     |                                                                             | 1: Enable                                                                          |
|     | (R/W)                                                                        | -                                                                                                                                           |
| 2   | HP_SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT                                     | Configures whether or not to enable Auto Decryption in Joint Download Boot mode.                                                          |
|     |                                                                             | 0: Disable                                                                         |
|     |                                                                             | 1: Enable                                                                          |
|     | (R/W)                                                                        | -                                                                                                                                           |
| 1   | HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT                                   | Configures whether or not to enable Manual Encryption in Joint Download Boot mode.                                                         |
|     |                                                                             | 0: Disable                                                                         |
|     |                                                                             | 1: Enable                                                                          |
|     | (R/W)                                                                        | -                                                                                                                                           |
```