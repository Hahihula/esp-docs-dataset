

```markdown
Figure 14.6-1. Two Ways to Access External Memory


## 14.6.1.1 Address

ESP32-C3’s flash can be further split to achieve more flexible permission control. Each split region can be configured with different access independently.

* Flash can be split into 4 regions, the length of each should be the integral multiples of 64 KB.
* Also, the starting address of each region should also be aligned to 64 KB.

The following registers can be used to configure how the flash is split.

Table 14.6-1. Split the External Memory into Split Regions

| Split Regions | Starting Address¹ | Split Region Configuration³ |
|---------------|-------------------|------------------------------|
| Flash Regionₙ (n: 0~3) | `SYSCON_FLASH_ACEn_ADDR_REG` | `SYSCON_FLASH_ACEn_SIZE_REG` |

---

¹ Configuring this field with the actual address, which should be aligned to 64 KB.
² When configuring the length of Regionₙ, note the total length of all flash regions should be no greater than 16 MB, respectively.
³ Each region cannot overlap with others.

## 14.6.1.2 Access Configuration

Each split region for flash can be configured with different permission independently via the register described in the table below.

Table 14.6-2. Access Configuration of Flash Regions

| Split Regions | Access Configuration Configuration Register | Cache   | SPI    |
|---------------|---------------------------------------------|---------|--------|
| Flash Regionₙ (n: 0 ~ 3) | `SYSCON_FLASH_ACEn_ATTR` | [1:0]ᴬ | [3:2]ᴮ |

---

ᴬ These bits are configured in order R/X. For example, configuring this field to 2'b10 indicates CACHE is granted with the read access but no instruction execution access to the Flash Regionₙ.
ᴮ These bits are configured in order W/R. For example, configuring this field to 2'b01 indicates SPI is granted with the read access but no write access to the Flash Regionₙ.
```