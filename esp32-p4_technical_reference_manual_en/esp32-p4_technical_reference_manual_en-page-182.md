

```markdown
| Field name | Bits | Description |
|------------|------|-------------|
| ioptions   | 6    | Indicates optional modes:<ul><li>sequentially inferred jumps (Bits 5): When set to 1, the targets of sequentially inferable jumps will not be reported. (This feature is not implemented, so bit 5 should always be 0)</li><li>branch prediction (Bit 4): When set to 1, the branch prediction is enabled. (This feature is not implemented, so bit 4 should always be 0)</li><li>jump target cache (Bit 3): When set to 1, the jump target cache is enabled. (This feature is not implemented, so bit 3 should always be 0)</li><li>full address (Bit 2):<ul><li>0: delta address mode</li><li>1: full address mode</li></ul></li><li>implicit exception (Bit 1): Exclude address from format 3 subformat 1 packet if trap vector can be determined from ecause. (This feature is not implemented, so bit 1 should always be 0)</li><li>implicit return (Bit 0): When set to 1, function return addresses will not be reported. (This feature is not implemented, bit 0 should always be 0)</li></ul>|
| sign_extend| 2    | Reserved |
```

### 2.6.3.2 Format 2 Packets

This packet contains only an instruction address, and is used when the address of an instruction must be reported (for example if the instruction is the target for an updiscon, or is the last instruction before exception), and there is no reported branch information.

The length is variable if delta address mode is enabled, ranging from 5 bytes to 8 bytes. The address field can be 8/16/24/32 bits, inferred from the packet length. For example, if the header length is *n* bytes, the address bits are *n − 4* bytes. A sign bit is required to extend the address field to 32 bits.

Table 2.6-6. Packet format 2

```markdown
| Field name | Bits | Description |
|------------|------|-------------|
| format     | 2    | 10 (addr-only): No branch information |
| notify      | 1    | If the value of this bit is different from the MSB of address, it indicates that this packet is reporting an instruction that is not the target of an uninferable discontinuity because a notification was requested via trigger[2] or a filter matched. |
| updiscon   | 1    | If the value of this bit is different from notify, it indicates that this packet is reporting the instruction following an uninferable discontinuity and is also the instruction before an exception, privilege change or resync. |
```