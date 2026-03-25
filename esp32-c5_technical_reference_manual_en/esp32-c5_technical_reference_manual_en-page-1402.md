

# 38.7 Registers

The addresses in this section are relative to CAN FD base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 38.1. TWAIFD_DEVICE_ID_VERSION_REG (0x0000)

<table><thead><tr><th>31</th><th>24</th><th>23</th><th>16</th><th>15</th><th>0</th></tr></thead><tbody><tr><td></td><td>0x2</td><td></td><td>0x4</td><td></td><td>Oxcafd<br>Reset</td></tr></tbody></table>

TWAIFD_DEVICE_ID Represents whether CAN IP function is mapped correctly on its base address. (RO)

TWAIFD_VER_MINOR Represents TWAI FD IP minor version. (RO)

TWAIFD_VER_MAJOR Represents TWAI FD IP major version. (RO)