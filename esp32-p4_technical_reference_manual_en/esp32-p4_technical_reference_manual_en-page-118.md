

```markdown
Register 1.93. uhwloop_state_reg (0x8C6)

| Bit Range | Description         |
|-----------|---------------------|
| 31        |                     |
|           | `0x00000000`        |
|           | Reset               |
|           | `0x0`               |

STATE Configures the state of the HWLP extension in user mode.
- `0x0`: OFF (Accessing HWLP instructions and CSRs will trigger an illegal instruction exception)
- `0x1`: INITIAL
- `0x2`: CLEAN
- `0x3`: DIRTY

Bits are physically the same as `mhwloop_state_reg`. Ensure the permission is enabled in `mh-wloop_state_reg.URW` field.

Assuming state is not OFF, whenever HWLP CSRs are modified, or HWLP instructions are executed, the state will be updated to DIRTY.
(R/W)
```