Title: Chapter 15 Permission Control (PMS)

Body Text:
- "2'b01: the second 16 KB"
- "2'b10: the third 16 KB"
- "2'b11: the fourth 16 KB"

Note under bullet points:
"Note that Block2 is only 32 KB, so you can only configure this field to 2'b00 or 2'b0 when Block2 is selected in the first step."

Example text with code snippets and instructions (formatted as code):
"For example, if you want to choose the first 16 KB of Internal SRAM1 Block3's as CPU0's trace memory, then
you need to:
- Write `0b0000010` to the PMS_INTERNAL_SRAM_COREO_TRACE USAGE field to select Block3
- Write `2'b00` to the PMS_INTERNAL_SRAM_COREO_TRACE_ALLOC field to select the first 16 KB."

Subtitle: Internal SRAM2 Access Configuration

Body Text:
"ESP32-S3's Internal SRAM2 includes Block9 and Block10 (see details in Table 15.3-3), which can be allocated
to either CPU/GDMA or DCACHE. Note that once configured, the configuration applies to both CPU0 and
CPU1.

ESP32-S3 uses registers described in Table 15.3-9 to configure the Internal SRAM2 for CPU/GDMA or 
DCACHE."

Table Title: Table 15.3-9. Internal SRAM2 Usage Configuration

Table:
| Block | PMS_INTERNAL_SRAM USAGE_1 REG |
|-------|--------------------------------|
| SRAM  | Block9B                        | [3] |
|       | Block10                        | [2] |

Notes for the table (formatted as code):
"A Set this bit to allocate a certain block to CPU/GDMA. Clear
this bit to allocate a certain block to DCACHE.
"B For example, setting this bit indicates Block9 is allocated to 
CPU/GDMA."

Text below Table 15.3-9:
"When a certain block is allocated to CPU/GDMA, ESP32-S3 uses the registers listed in Table 15.3-10
to configure the write (W) and read (R) accesses of CPU's DBUS, from the Secure World and Non-secure World,
to this block:

Table Title: Table 15.3-10. Access Configuration to Internal SRAM2

Table:
| Bus A | From World | Configuration Registers |
|-------|------------|-------------------------|
|       |            | PMS_CORE_XDRAMO_PMS CONSTRAIN_1 REG [9:8] C [11:10] W/R |
| DBUS  |            | PMS_CORE_XDRAMO_PMS CONSTRAIN_1 REG [21:20] [23:22] W/R |
| GDMA  | XX Peripherals B | PMS_DMA_APBPERI_XX_PMS CONSTRAIN_1 REG [9:8] C [11:10] W/R |

Notes for the table (formatted as code):
"A To access the Internal SRAM2, the CPU/GDMA must be configured with both the usage permission and respective
access permission.
"B 1: with access; O: without access

C For example, configuring this field to `0b10` indicates CPU's DBUS is granted with write access but not read access 
from the Secure World to the Block9 of Internal SRAM2."

Footer:
"Espressif Systems
691 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback"

Navigation Link: GoBack