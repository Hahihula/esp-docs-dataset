**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

---

**Body Text:**

Table 3.4-3 lists the requirements for descriptor field alignment when GDMA accesses internal RAM. Size, length, and buffer address pointer in transmit descriptors do not need to be aligned. However, size and buffer address pointer in receive descriptors except length should be aligned with block size. Table 3.4-4 illustrates the value of `GDMA_IN_EXT_MEM_BK_SIZE_CHn` or `GDMA_OUT_EXT_MEM_BK_SIZE_CHn` bit when fields in linked list descriptors are 16-byte, 32-byte and 64-byte aligned respectively.

**Table Title:**
Table 3.4-4. Relationship Between Configuration Register, Block Size and Alignment

| GDMA_IN_EXT_MEM_BK_SIZE_CHn or GDMA_OUT_EXT_MEM_BK_SIZE_CHn | Block Size   | Alignment          |
|-------------------------------------------------------------|--------------|--------------------|
| 0                                                            | 16 bytes     | 16-byte aligned    |
| 1                                                            | 32 bytes     | 32-byte aligned    |
| 2                                                            | 64 bytes     | 64-byte aligned    |

**Note:**
For receive descriptors, if the data length received are not aligned with block size, GDMA will pad the data received with 0 until they are aligned to initiate burst transfer. You can read the length field in receive descriptors to obtain the length of valid data received.

---

**Subsection Title:**
3.4.10 External RAM Access Permissions

**Body Text:**

GDMA in ESP32-S3 has a permission control module for access to external RAM. As Figure 3.4-4 shows, the permission control module divides the 32 MB external RAM into four areas through three configurable boundaries, namely boundary 0, boundary 1, and boundary 2.

- **Area 0:** `0x3C000000 ~ boundary 0 (include 0x3C000000 but exclude boundary 0)`
- **Area 1:** boundary 0 ~ boundary 1 (include boundary 0 but exclude boundary 1)
- **Area 2:** boundary 1 ~ boundary 2 (include boundary 1 but exclude boundary 2)
- **Area 3:** boundary 2 ~ `0x3DFFFFF` (include boundary 0)

Boundary 0, 1, and 2 are configured via `PMS_EDMA_BOUNDARY_0`, `PMS_EDMABOUNDARY_1`, and `PMS_EDMABOUNDARY_2`, respectively. For details about these fields, please refer to Chapter 15 Permission Control (PMS). The unit of these fields is 4 KB. For example, if `PMS_EDMABOUNDARY_0` is `0x80`, the address of boundary 0 should be `0x3C00000 + 0x80 * 4 KB = 3c080000`, in which `0x3C000000` is the starting address of accessible external RAM.

**Figure Title:**
Figure 3.4-4. Dividing External RAM into Areas

---

**Footer Text:**

Espressif Systems  
Page number and document version information (not specified)