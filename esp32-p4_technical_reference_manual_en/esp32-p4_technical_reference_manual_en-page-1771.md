

```markdown
Register 37.3. PPA_CLUT_CONF_REG (0x000C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             | (reserved)                                                                  |
| 30  |                                             | Reset                                                                       |
| 29  |                                             | PPA_BLENDO_CLUT_MEM_CLK_ENA                                                 |
| 28  |                                             | PPA_BLENDO_CLUT_MEM_FORCE_PU                                                |
| 27  |                                             | PPA_BLENDO_CLUT_MEM_FORCE_PD                                                |
| 26  |                                             | PPA_BLENDO_CLUT_MEM_RDADDR_RST                                              |
| 25  |                                             | PPA_BLENDO_CLUT_MEM_RST                                                     |
| 24  |                                             | PPA_BLEND1_CLUT_MEM_CLK_ENA                                                 |
| 23  |                                             | PPA_BLEND1_CLUT_MEM_FORCE_PU                                                |
| 22  |                                             | PPA_BLEND1_CLUT_MEM_FORCE_PD                                                |
| 21  |                                             | PPA_BLEND1_CLUT_MEM_RDADDR_RST                                              |
| 20  |                                             | PPA_BLEND1_CLUT_MEM_RST                                                     |
| 19  |                                             | PPA_APB_FIFO_MASK                                                            |

PPA_APB_FIFO_MASK Configures the access mode of BLEND CLUT.
- 1'b0: Access CLUT in FIFO mode. For details, please refer to [37.5.1.2](#).
- 1'b1: Access CLUT in MEM mode. For details, please refer to [37.5.1.2](#).

(R/W)

PPA_BLENDO_CLUT_MEM_RST Configures whether to reset BLENDO CLUT.
- 0: Release reset
- 1: Reset

(R/W)

PPA_BLEND1_CLUT_MEM_RST Configures whether to reset BLEND1 CLUT.
- 0: Release reset
- 1: Reset

(R/W)

PPA_BLENDO_CLUT_MEM_RDADDR_RST Configures whether to reset BLENDO CLUT read address in FIFO mode.
- 0: Release reset
- 1: Reset

(R/W)

PPA_BLEND1_CLUT_MEM_RDADDR_RST Configures whether to reset BLEND1 CLUT read address in FIFO mode.
- 0: Release reset
- 1: Reset

(R/W)

PPA_BLENDO_CLUT_MEM_FORCE_PD Configures whether to enable the force power down of BLEND CLUT.
- 0: Disable
- 1: Enable

(R/W)

Continued on the next page...
```