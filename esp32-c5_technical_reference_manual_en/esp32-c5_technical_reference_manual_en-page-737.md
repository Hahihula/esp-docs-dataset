

```markdown
| Slaves Masters | ROM | HP SRAM | LP SRAM | HP_CPU_PERI¹ | HP_PERI² | LP_PERI³ | EXT MEM⁴ |
|----------------|-----|----------|----------|---------------|-----------|-----------|------------|
| HP CPU        | PMP | PMP+ CPU_APM | PMP + LP_APM/ LP_APMO | PMP + HP_APM + PERI_APM | HP_APM + PERI_APM | PMP + LP_APM + PERI_APM | PMP |
| LP CPU        | N/A | HP_APM   | LP_APM/ LP_APMO | N/A           | HP_APM + PERI_APM | LP_APM + PERI_APM | N/A       |
| GDMA          | N/A | HP_APM   | LP_APM/ LP_APMO | N/A           | N/A       | N/A       | HP_APM     |
| Other masters⁵ | N/A | HP_APM   | LP_APM/ LP_APMO | N/A           | N/A       | N/A       | N/A        |

```