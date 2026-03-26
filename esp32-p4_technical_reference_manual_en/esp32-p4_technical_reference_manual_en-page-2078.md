

# 40.9 Registers

The addresses in this section are relative to CSI Host base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 40.1. CSI_HOST_VERSION_REG (0x0000)

```
31                                 0
+---------------------------------------------------------------+
|                CSI_HOST_VERSION                                |
+---------------------------------------------------------------+
```

**CSI_HOST_VERSION** Version control register. (RO)

---

## Register 40.2. CSI_HOST_N_LANES_REG (0x0004)

```
31                                 0
+---------------------------------------------+
| (reserved)                                   |   3    2     0
|                                          +----+----+----+
|                                          | 0x1 | Reset |
+---------------------------------------------+
```

**CSI_HOST_N_LANES** Configures the number of active lanes that the MIPI CSI-2 host uses to receive the camera device data. This can only be updated when the RX D-PHY lane is in stop state.

- 0: Data lane 0 is active
- 1: Both data lane 0 and data lane 1 are active

Other values: Invalid

(R/W)