

# 1.7 Memory-Mapped Registers

## 1.7.1 Overview

The tightly-coupled memory-mapped registers below are present within the core complex:

* CLIC registers
* CLINT registers

## 1.7.2 Features

HP CPU core supports:

* Access to CLIC registers
* Bus-error exception generation on invalid address access
* Access to CLINT registers

## 1.7.3 Functional Description

The table below shows the address decoding used by HP core to access CLIC and CLINT address range.

Table 1.7-1. Address Decoding for Memory-Mapped Register Access

| Bits | Description |
|------|-------------|
| 31:28 | Fixed as 0x2, i.e. base address |
| 27:20 | Identifies the sub module:<br>0x0: CLINT<br>0x8: CLIC<br>0xB: CLIC user<br>Others: Reserved |
| 19:16 | Controls access type:<br>0x0: Access own registers<br>0x1: Reserved |
| 15:0 | Register offset |

Table 1.7-2. Internal Memory Address Map

| Block | Start Address | End Address |
|-------|---------------|-------------|
| CLINT | 0x20000000    | 0x2000FFFF |
| CLIC  | 0x20800000    | 0x2080FFFF |