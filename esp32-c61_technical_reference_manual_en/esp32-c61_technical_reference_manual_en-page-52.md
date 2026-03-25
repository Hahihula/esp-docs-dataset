

```markdown
| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| TW  | Represents whether the WFI (wait for interrupt) instruction can execute in less privileged modes. <br> O: WFI can execute in lower privilege modes. <br> 1: WFI can only be executed in machine mode, and if executed in a less privileged mode, it will trigger an illegal instruction exception. (RO) |
| MPRV | Represents whether to apply `ustatus.MPP` as the effective privilege mode, in which loads and stores execute, instead of the actual privilege mode in which the CPU is executing. <br> O: Not apply <br> 1: Apply <br> Note that instruction protection is unaffected by this bit. (RO) |
| MPP | Represents machine previous privilege mode (before trap). <br> `0x0`: User mode <br> `0x3`: Machine mode (RO) |
```