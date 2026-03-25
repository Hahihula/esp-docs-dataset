

```markdown
- KEYMNG_INTR
- HUK_INTR
```

There are several internal interrupt sources from Key Manager and HUK Generator that can generate the above interrupt signals. The interrupt sources from Key Manager and HUK Generator are listed with their trigger conditions and the resulted interrupt signals in Table 31.9-1.

Table 31.9-1. Key Manager and HUK Generator's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                                                                 | Interrupt Signal |
|----------------------------|------------------------------------------------------------------------------------|------------------|
| KEYMNG_PREP_DONE_INT       | Completion of Key Manager's PREP phase                                            | KEYMNG_INTR      |
| KEYMNG_PROC_DONE_INT       | Completion of Key Manager's PROC phase                                             | KEYMNG_INTR      |
| KEYMNG_POST_DONE_INT       | Completion of Key Manager's POST phase                                             | KEYMNG_INTR      |
| HUK_PREP_DONE_INT          | Completion of HUK Generator's PREP phase                                          | HUK_INTR         |
| HUK_PROC_DONE_INT          | Completion of HUK Generator's PROC phase                                          | HUK_INTR         |
| HUK_POST_DONE_INT          | Completion of HUK Generator's POST phase                                          | HUK_INTR         |

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 11 Interrupt Matrix > Section 11.2 Terminology.

## 31.10 Memory Blocks

The addresses in this section are relative to Key Manager or HUK Generator base address provided in Table 6.3-2 in Chapter 6 System and Memory.

Table 31.10-1. Key Manager Memory Blocks

| Name                        | Description                                                                 | Size (byte) | Starting Address | Ending Address | Access   |
|------------------------------|-----------------------------------------------------------------------------|-------------|------------------|----------------|----------|
| KEYMNG_ASSIST_INFO_MEM      | Stores assistant information                                               | 64          | 0x0100           | 0x013F         | Varies   |
| KEYMNG_PUBLIC_INFO_MEM      | Stores public information                                                  | 64          | 0x0140           | 0x017F         | Varies   |
| KEYMNG_SW_INIT_KEY_MEM      | Stores sw_init_key                                                         | 32          | 0x0180           | 0x019F         | Varies   |

Table 31.10-2. HUK Generator Memory Blocks

| Name        | Description     | Size (byte) | Starting Address | Ending Address | Access   |
|-------------|-----------------|-------------|------------------|----------------|----------|
| HUK_INFO_MEM| Stores huk_info | 384         | 0x0100           | 0x027F         | Varies   |

## 31.11 Register Summary
```