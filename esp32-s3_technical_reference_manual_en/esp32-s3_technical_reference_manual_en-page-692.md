**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Section Titles and Subsections with Content:**

### 15.3.3 RTC FAST Memory

#### 15.3.3.1 Address
ESP32-S3’s RTC FAST Memory is 8 KB. See the address of RTC FAST Memory below:

| **Memory** | **Starting Address** | **Ending Address** |
|-------------|----------------------|--------------------|
| RTC FAST Memory | 0x600F_E000 | 0x600F_FFF |

#### 15.3.3.2 Access Configuration
ESP32-S3’s RTC FAST Memory can be further split into two regions. Each split region can be configured independently with different access by configuring respective registers (PMS CORE, PIF, PMS CONSTRAIN_0, REG).

Note that split regions can be configured independently for CPU0 and CPU1 and for the Secure World and Non-secure World.

The Register for configuring the split line is described below:

**Table 15.3-12: Split RTC FAST Memory into the Higher Region and the Lower Region**

| **Memory** | **Split Regions** | **Configuration Register** |
|-------------|--------------------|---------------------------|
| RTC FAST Memory | Higher Region, Lower Region | PIF_PMS CONSTRAIN_9_REG [10:0], PIF_PMS CONSTRAIN_9_REG [21:11] |

1. The offset from the RTC FAST Memory base address should be used when configuring the split address.
   - For example, if you want to split the RTC FAST Memory at 0x600F_F000, then write 0x1000 to this register.

Access configuration for the higher and lower regions of the RTC FAST MEMORY is described below:

**Table 15.3-13: Access Configuration to the RTC FAST Memory**

| **RTC Bus** | **FAST Memory** | **Secure World** | **Non-secure World** |
|-------------|-----------------|------------------|----------------------|
| Peri Bus (PIF) Higher Region | PIF_PMS CONSTRAIN_10_REG [5:3] B | Non-secure World X/W/R |
| Peri Bus (PIF) Lower Region | PIF_PMS CONSTRAIN_10_REG [2:0] | |

A. 1 with access; O: without access
B. For example, configuring this field to Ob1 indicates CPU’s peripheral (PIF) bus is granted with the instruction execution and read accesses but not the read access from the Secure WORLD to the higher region of RTC FAST Memory.

### 15.3.4 RTC SLOW Memory

#### 15.3.4.1 Address
ESP32-S3’s RTC SLOW Memory is 8 KB. This memory can be accessed using two addresses, i.e., RTCSlow_0 and RTCSlow_1. See details in Table 15.3-14 below:

**Table Reference:**
See the table for more information on accessing different parts of the memory.

---

**Footer Information:**  
Espressif Systems  
692 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback