

```markdown
| Name         | Description                  | Address | Access |
|--------------|------------------------------|---------|--------|
| tselect      | Trigger Select Register      | 0x7A0   | R/W    |
| tdata1       | Trigger Abstract Data 1      | 0x7A1   | R/W    |
| tdata2       | Trigger Abstract Data 2      | 0x7A2   | R/W    |
| tcontrol     | Global Trigger Control       | 0x7A5   | R/W    |

### 1.7.5 Register Description

#### Register 1.22. tselect (0x7A0)

```
31                                 3 2      0
+-----------------------------------------------+
|                0x00000000                 |
+-----------------------------------------------+
```

tselect Index (0-7) of the selected trigger unit. (R/W)

#### Register 1.23. tdata1 (0x7A1)

```
31      28 27 26                         0
+-------------------------------+
|           0x2                 | Reset
+-------------------------------+
```

**type** Type of trigger. (RO)  
This field is reserved since only match type (0x2) triggers are supported.

**dmode** This is set to 1 if a trigger is being used by the debugger. (R/W *)  

- 0: Both Debug and M-mode can write the tdata1 and tdata2 registers at the selected tselect.
- 1: Only Debug Mode can write the tdata1 and tdata2 registers at the selected tselect. Writes from other modes are ignored.

*Note : Only writable from debug mode.

**data** Abstract tdata1 content. (R/W)  
This will always be interpreted as fields of mcontrol since only match type (0x2) triggers are supported.
```