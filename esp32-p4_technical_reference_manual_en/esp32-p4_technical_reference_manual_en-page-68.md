

```markdown
| Name       | Description                                                                 | Address | Access |
|------------|-----------------------------------------------------------------------------|---------|--------|
| stpc0      | Store bus error PC register 0                                                | 0xBF0   | R/W    |
| stpc1      | Store bus error PC register 1                                                | 0xBF1   | R/W    |
| stpc2      | Store bus error PC register 2                                                | 0xBF2   | R/W    |
| sttval0    | Store bus error access address register 0                                   | 0xBF8   | R/W    |
| sttval1    | Store bus error access address register 1                                   | 0xBF9   | R/W    |
| sttval2    | Store bus error access address register 2                                   | 0xBFA   | R/W    |

Note that if write/set/clear operation is attempted on any of the CSRs which are read-only (RO), as indicated in the above table, the CPU will generate an illegal instruction exception.

### 1.5.2 Register Description

#### Register 1.1. mvendorid (0xF11)

```
MVENDORID
31                                 0
+----------------------------------+
|          0x00000612               |
+----------------------------------+
Reset
```

**MVENDORID** Represents Vendor ID. (RO)

#### Register 1.2. marchid (0xF12)

```
MARCHID
31                                 0
+----------------------------------+
|          0x80000003               |
+----------------------------------+
Reset
```

**MARCHID** Represents Architecture ID. (RO)

#### Register 1.3. mimpid (0xF13)

```
MIMPID
31                                 0
+----------------------------------+
|          0x00000001               |
+----------------------------------+
Reset
```

**MIMPID** Represents Implementation ID. (RO)
```