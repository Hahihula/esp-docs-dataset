

# 1.8 Memory-Mapped Registers

## 1.8.1 Overview

The tightly-coupled memory-mapped registers below are present within the core complex:

* CLIC registers for each HP core  
* Shared CLINT registers  

### 1.8.2 Features

Each HP CPU core supports:  

* Access to the other HP core's CLIC registers  
* Bus-error exception generation on invalid address access  
* Access to CLINT registers. However, only Core O can modify CLINT timer value  

## 1.8.3 Functional Description

The table below shows the address decoding used by each HP core to access CLIC and CLINT address range.

Table 1.8-1. Address Decoding for Memory-Mapped Register Access

| Bits | Description |
|------|-------------|
| 31:28 | Fixed as 0x2, i.e. base address |
| 27:20 | Identifies the sub module:<br>0x0: CLINT<br>0x08: CLIC<br>0xB: CLIC user<br>Others: Reserved |
| 19:16 | Controls access type:<br>0x0: Access own registers<br>0x1: Access the other core's registers |
| 15:0 | Register offset |

Table 1.8-2. Internal Memory Address Map

| Block           | Start Address | End Address   |
|-----------------|---------------|---------------|
| CLINT (Self)    | 0x20000000    | 0x2000FFFF    |
| CLIC (Self)     | 0x20800000    | 0x2080FFFF    |
| CLINT (Other Core) | 0x20010000   | 0x2001FFFF    |
| CLIC (Other Core) | 0x20810000   | 0x2081FFFF    |