

# Chapter 22

## LP Mailbox

### 22.1 Overview

ESP32-P4 integrates an LP Mailbox module which provides an efficient inter-core communication mechanism between the LP CPU and HP CPU0/1. The LP Mailbox module comprises of sixteen 32-bit message registers that the LP CPU and HP CPU0/1 can use to store and exchange message. Inter-core communication between LP CPU and HP CPU0/1 is achieved through an interrupt mechanism implemented within the LP Mailbox module.

### 22.2 Features

ESP32-P4 LP Mailbox has the following features:

* Sixteen 32-bit message registers for inter-core communication
* LP CPU external interrupt signal: MB_LP_INTR
* HP CPUx (x: 0 ~ 1) external interrupt signal: MB_HP_INTR