

# 24.4 Memory Summary

The addresses in this section are relative to the Digital Signature base address provided in Table 5.3-2 in Chapter 5 System and Memory.

| Name         | Description          | Size (byte) | Starting Address | Ending Address | Access |
|--------------|----------------------|-------------|------------------|----------------|--------|
| DS_Y_MEM     | Memory block Y       | 384         | 0x0000           | 0x017F         | WO     |
| DS_M_MEM     | Memory block M       | 384         | 0x0200           | 0x037F         | WO     |
| DS_RB_MEM    | Memory block r̄      | 384         | 0x0400           | 0x057F         | WO     |
| DS_BOX_MEM   | Memory block Box     | 48          | 0x0600           | 0x062F         | WO     |
| DS_X_MEM     | Memory block X       | 384         | 0x0800           | 0x097F         | WO     |
| DS_Z_MEM     | Memory block Z       | 384         | 0x0A00           | 0x0B7F         | RO     |