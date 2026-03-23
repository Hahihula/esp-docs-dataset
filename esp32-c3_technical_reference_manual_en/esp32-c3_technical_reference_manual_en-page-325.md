

```markdown
As seen above, GDMA’s peripheral region is divided into 7 split regions (implemented in hardware), which can be configured with different permission independently, thus achieving independent permission control for each GDMA channel.

Users can configure CPU’s read (R) and write (W) accesses to a specific split region (Peri Regionn) in the privileged environment and in the unprivileged environment by configuring PMS_REGION_PMS_CONSTRAN_n_REG.

Notes on PMS_REGION_PMS_CONSTRAN_n_REG:

• n can be 1~10, in which
    - PMS_REGION_PMS_CONSTRAN_1_REG is for configuring CPU’s permission in the privileged environment.
    - PMS_REGION_PMS_CONSTRAN_2_REG is for configuring CPU’s permission in the unprivileged environment.
    - PMS_REGION_PMS_CONSTRAN_n_REG (n = 3~10) are used to configuring the starting addresses for each Peri Regions. Note the starting address of each Peri Region is also the ending address of the previous Peri Region.

Table 14.5-2. Access Configuration of Peri Regions

| Peri Regions | Starting Address Configuration | Access Configuration Privileged Environment | Unprivileged Environment |
|--------------|----------------------------------|-------------------------------------------------------------|---------------------------|
|              |                                  |                                                     |                           |
| Peri Region0 | PMS_REGION_PMS_CONSTRAN_3_REG    | PMS_REGION_PMS_CONSTRAN_1_REG [1:0]                       | PMS_REGION_PMS_CONSTRAN_2_REG [1:0] |
| Peri Region1 | PMS_REGION_PMS_CONSTRAN_4_REG    | PMS_REGION_PMS_CONSTRAN_1_REG [3:2]                       | PMS_REGION_PMS_CONSTRAN_2_REG [3:2] |
| Peri Region2 | PMS_REGION_PMS_CONSTRAN_5_REG    | PMS_REGION_PMS_CONSTRAN_1_REG [5:4]                       | PMS_REGION_PMS_CONSTRAN_2_REG [5:4] |
| Peri Region3 | PMS_REGION_PMS_CONSTRAN_6_REG    | PMS_REGION_PMS_CONSTRAN_1_REG [7:6]                       | PMS_REGION_PMS_CONSTRAN_2_REG [7:6] |
| Peri Region4 | PMS_REGION_PMS_CONSTRAN_7_REG    | PMS_REGION_PMS_CONSTRAN_1_REG [9:8]                       | PMS_REGION_PMS_CONSTRAN_2_REG [9:8] |
| Peri Region5 | PMS_REGION_PMS_CONSTRAN_8_REG    | PMS_REGION_PMS_CONSTRAN_1_REG [11:10]                     | PMS_REGION_PMS_CONSTRAN_2_REG [11:10] |
| Peri Region6*| PMS_REGION_PMS_CONSTRAN_9_REG    | PMS_REGION_PMS_CONSTRAN_1_REG [13:12]                     | PMS_REGION_PMS_CONSTRAN_2_REG [13:12] |

* The ending address of Peri Region6 is configured by PMS_REGION_PMS_CONSTRAN_10_REG.

## 14.6 External Memory

ESP32-C3 can access the external memory via one of the two ways illustrated in Figure 14.6-1 below.
• CPU via SPI1
• CPU via CACHE

Where,
• Box 0 checks the SPI and Cache’s access to external flash.
• Box 1 checks CPU’s access to Cache.

### 14.6.1 SPI and Cache’s Access to External Flash
```