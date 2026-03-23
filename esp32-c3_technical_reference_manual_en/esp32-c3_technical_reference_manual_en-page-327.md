

```markdown
## 14.6.2 CPU's Access to Cache

ESP32-C3’s CPU access Cache using a virtual address. The memory space in ESP32-C3 that is accessible for CPU to access Cache is called "Virtual Address Region", which can be seen in Table 14.6-3 below.

Table 14.6-3. Cache Virtual Address Region

| Bus Type | Virtual Address Region Starting Address | Ending Address | Size (MB) | Target |
|----------|-----------------------------------------|----------------|-----------|--------|
| DBus (read-only) | 0x3C00_0000 | 0x3C7F_FFFF | 8 | Uniform Cache |
| IBus | 0x4200_0000 | 0x427F_FFFF | 8 | Uniform Cache |

### 14.6.2.1 Split Regions

Both ESP32-C3’s DBUS and IBUS Cache virtual address regions can be further split into up to 4 regions. Users can configure different access to each region independently.

Table 14.6-4. Split IBUS Cache Virtual Address into 4 Regions

| Split Regions¹ | Starting Address | Split Region Configuration Ending Address |
|----------------|------------------|---------------------------------------------|
| IBUS Region0   | 0x4200_0000      | `EXTMEM_IBUS_PMS_TBL_BOUNDARY0_REG`²       |
| IBUS Region1   | `EXTMEM_IBUS_PMS_TBL_BOUNDARY0_REG`+1 | `EXTMEM_IBUS_PMS_TBL_BOUNDARY1_REG`²     |
| IBUS Region2   | `EXTMEM_IBUS_PMS_TBL_BOUNDARY1_REG`+1 | `EXTMEM_IBUS_PMS_TBL_BOUNDARY2_REG`²     |
| IBUS Region3   | `EXTMEM_IBUS_PMS_TBL_BOUNDARY2_REG`+1 | 0x4280_0000 |

¹ The address range of each split region is [Starting Address, Ending Address).  
² The address represented is "0x4200_0000 + 0x1000 * `EXTMEM_IBUS_PMS_TBL_BOUNDARYn_REG`". For example, when `EXTMEM_IBUS_PMS_TBL_BOUNDARY0_REG` is configured to 2, then the address range of IBUS Region0 is [0x4200_0000, 0x4200_2000).

Table 14.6-5. Split DBUS Cache Virtual Address into 4 Regions

| Split Regions¹ | Starting Address | Split Region Configuration Ending Address |
|----------------|------------------|---------------------------------------------|
| DBUS Region0   | 0x3C00_0000      | `EXTMEM_DBUS_PMS_TBL_BOUNDARY0_REG`²       |
| DBUS Region1   | `EXTMEM_DBUS_PMS_TBL_BOUNDARY0_REG`+1 | `EXTMEM_DBUS_PMS_TBL_BOUNDARY1_REG`²     |
| DBUS Region2   | `EXTMEM_DBUS_PMS_TBL_BOUNDARY1_REG`+1 | `EXTMEM_DBUS_PMS_TBL_BOUNDARY2_REG`²     |
| DBUS Region3   | `EXTMEM_DBUS_PMS_TBL_BOUNDARY2_REG`+1 | 0x3C80_0000 |

¹ The address range of each split region is [Starting Address, Ending Address).  
² The address represented is "0x3C00_0000 + 0x0100 * `EXTMEM_DBUS_PMS_TBL_BOUNDARYn_REG`". For example, when `EXTMEM_DBUS_PMS_TBL_BOUNDARY2_REG` is configured to 2, then the address range of IBUS Split Region0 is [0x3C00_0000, 0x3C00_0200)].

### 14.6.3 Access Configuration

Each Cache split region can be configured with different permission independently via registers described in Table 14.6-6 and Table 14.6-7 below.
```