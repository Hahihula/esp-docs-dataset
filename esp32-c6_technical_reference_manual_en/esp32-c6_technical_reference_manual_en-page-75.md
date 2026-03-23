

```markdown
Register 1.36. dpc (0x7B1)

dpc Upon entry to debug mode, dpc is written with the virtual address of the instruction that encountered the exception. When resuming, the CPU core's PC is updated to the virtual address stored in dpc. A debugger may write dpc to change where the CPU resumes. (R/W)


Register 1.37. dscratch0 (0x7B2)

dscratch0 Used by Debug Module internally. (R/W)


Register 1.38. dscratch1 (0x7B3)

dscratch1 Used by Debug Module internally. (R/W)
```