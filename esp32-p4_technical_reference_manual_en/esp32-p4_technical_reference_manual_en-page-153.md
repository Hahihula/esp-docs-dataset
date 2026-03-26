

```markdown
| Name     | Description                                                                 | Address | Access |
|----------|-----------------------------------------------------------------------------|---------|--------|
| dmcs2    | Debug module control and status register 2                                 | 0x32    | R/W    |

### 1.11.2.5 Register Description

Register 1.124. dmcs2 (0x32)

```

```plaintext
31          12   11   10        7      6       group     hgwrite hgselect
+-----------+------+------+------+------+----------+----------+--------+
|           | 0    | 0    |         | Reset |
+-----------+------+------+------+------+----------+----------+--------+
```

**groupType** Configures the group type.
- O (halt group): The remaining fields in this register configure halt groups
- 1 (resume group): The remaining fields in this register configure resume groups
(R/W)

**dmexttrigger** Configures the currently selected DM external trigger. If a non-existent trigger value is written here, the hardware will change it to a valid value or O if no DM external triggers exist.
(R/W)

**group** When hgselect is O, this field contains the group of the hart specified by hartsel.
When hgselect is 1, this field contains the group of the DM external trigger selected by dmext-trigger.
The value written to this field is ignored unless hgwrite is also written 1.
Group numbers are contiguous starting from O, with the highest number being implementation-dependent, and possibly different between different group types. Debuggers should read back this field after writing to confirm they are using a supported hart group. If groups are not implemented, this entire field is O.
(R/W)

**hgwrite** When 1 is written and hgselect is O, for every selected hart, the DM will change its group to the value written to group, if the hardware supports that group for that hart. Implementations may also change the group of a minimal set of unselected harts in the same way, if that is necessary due to a hardware limitation. When 1 is written and hgselect is 1, the DM will change the group of the DM external trigger selected by dmexttrigger to the value written to group, if the hardware supports that group for that trigger. Writing O has no effect.
(R/W)

**hgselect** Tied to zero.
- O: Operate on HART
(RO)
```