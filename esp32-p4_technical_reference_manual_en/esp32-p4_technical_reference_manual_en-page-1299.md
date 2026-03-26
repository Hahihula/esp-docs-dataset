

```markdown
Chapter 20 System Registers (SYSREG)

Register 20.66. HP_SYSTEM_L2_MEM_ERR_RESP_CTRL_REG (0x0198)
```

![HP_SYSTEM_L2_MEM_ERR_RESP_CTRL_REG bitfield diagram](image_description: A horizontal bitfield diagram labeled with "reserved" at the top, showing bits from 31 to 0, where only bit 0 is labeled as HP_SYSTEM_L2_MEM_ERR_RESP_EN. The rightmost column indicates a reset value of 0.)

```markdown
HP_SYSTEM_L2_MEM_ERR_RESP_EN Configures whether or not to report ECC error to the HP CPU and trigger exception.

O: Disable  
1: Enable  
(R/W)
```

Register 20.67. HP_SYSTEM_L2_MEM_AHB_BUFFER_CTRL_REG (0x019C)

![HP_SYSTEM_L2_MEM_AHB_BUFFER_CTRL_REG bitfield diagram](image_description: A horizontal bitfield diagram labeled with "reserved" at the top, showing bits from 31 to 0, where only specific bits are defined. The rightmost column indicates a reset value of 0 for both relevant fields.)

```markdown
HP_SYSTEM_L2_MEM_AHB_WRBUFFER_EN Configures whether or not to enable L2MEM AHB write buffer.

O: Disable  
1: Enable  
(R/W)

HP_SYSTEM_L2_MEM_AHB_RDBUFFER_EN Configures whether or not to enable L2MEM AHB read buffer.

O: Disable  
1: Enable  
(R/W)
```

Espressif Systems

Submit Documentation Feedback

ESP32-P4 TRM
PRELIMINARY
```