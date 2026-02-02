**Chapter Title:**
Chapter 3 System and Memory

**GoBack Link:** GoBack

---

**Table Header (with values):**
- Data: 0x3F80_0000, Boundary Address: Ox3FBF_FFFF, Size: 4 MB, External SRAM
- Bus Type: Low Address, High Address: OX40BF_FFFF, Target: Read and Write

**Instruction Header (with values):**
- Instruction: 0x400C_2000, Size: KB, Comment: Internal Flash/Read

---

**Section Title:** 
3.3.4 Cache

**Body Text:**
As shown in Figure 3.3-1, each of the two CPUs in ESP32 has 32 KB of cache featuring a block size of 32 bytes for accessing external storage. PRO CPU uses bit PRO_CACHE_ENABLE in register DPORO_PRO_CACHE_CTRLto enable the Cache, while APP CPU uses bit APP_CACHE_ENABLE in register DPORO_APP_CACHE_CTRLto enable the same function.

**Figure Caption:**
Figure 3.3-1. Cache Block Diagram

**Diagram Description (with labels):**
PRO CPU and APP CPU are connected to external memory through Cache0 and Cache1 respectively, with a SWAP instruction bus between them.
- PRO_CACHE_ENABLE
- CACHE_MUX_MODE
- POOL0/POOL1: Each 32KB block is labeled as such.

**Additional Text:** 
ESP32 uses a two-way set-associative cache. When the Cache function is to be used either by PRO CPU or APP CPU, bit CACHE_MUX_MODE[1:0] in register DPORO_CACHE_MUX_MODE_REG can be set to select POOL0 or POOL1 in the Internal SRAMO as the cache memory. When both PRO CPU and APP CPU use the Cache function, POOL0 and POOL1 in the Internal SRAM will be used simultaneously as the cache memory while they can also be used by the instruction bus.

**Table Title:**
Table 3.3-5. Cache memory mode

**Table Content (with headers):**
| CACHE_MUX_MODE | POOLO | POOL1 |
|----------------|-------|-------|
| PRO CPU        |       | APP CPU |
| PRO CPU/APP CPU|       |       |
| APP CPU        |       | PRO CPU |

**Additional Text:**
As described in table 3.3-5, when bit CACHE_MUX_MODE is set to 1 or 2, PRO CPU and APP CPU cannot enable the Cache function at the same time. When the Cache function is enabled, POOLO or POOL1 can only

---

**Footer Information:** 
Espressif Systems
ESP32 TRM (Version 5.6)
71 Submit Documentation Feedback