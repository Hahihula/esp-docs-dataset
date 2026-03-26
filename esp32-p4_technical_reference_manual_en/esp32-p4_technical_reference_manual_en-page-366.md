

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| DMAC_INTSTATUSO_REG                        | VDMA interrupt status register                                              | 0x0030  | RO     |
| DMAC_COMMONREG_INTCLEARO_REG               | VDMA common interrupt clear register                                       | 0x0038  | WO     |
| DMAC_COMMONREG_INTSTATUS_ENABLEO_REG       | VDMA common interrupt status enable register                               | 0x0040  | varies |
| DMAC_COMMONREG_INTSIGNAL_ENABLEO_REG       | VDMA common interrupt signal enable register                               | 0x0048  | varies |
| DMAC_COMMONREG_INTSTATUSUSO_REG             | VDMA common interrupt status register                                      | 0x0050  | RO     |
| DMAC_CH1_INTSTATUS_ENABLEO_REG             | VDMA channel 1 interrupt status enable register                            | 0x0180  | varies |
| DMAC_CH1_INTSTATUSUSO_REG                  | VDMA channel 1 interrupt status register                                   | 0x0188  | RO     |
| DMAC_CH1_INTSIGNAL_ENABLEO_REG             | VDMA channel 1 interrupt signal enable register                            | 0x0190  | varies |
| DMAC_CH1_INTCLEARO_REG                     | VDMA channel 1 interrupt clear register                                    | 0x0198  | WO     |
| DMAC_CH2_INTSTATUS_ENABLEO_REG             | VDMA channel 2 interrupt status enable register                            | 0x0280  | varies |
| DMAC_CH2_INTSTATUSUSO_REG                  | VDMA channel 2 interrupt status register                                   | 0x0288  | RO     |
| DMAC_CH2_INTSIGNAL_ENABLEO_REG             | VDMA channel 2 interrupt signal enable register                            | 0x0290  | varies |
| DMAC_CH2_INTCLEARO_REG                     | VDMA channel 2 interrupt clear register                                    | 0x0298  | WO     |
| DMAC_CH3_INTSTATUS_ENABLEO_REG             | VDMA channel 3 interrupt status enable register                            | 0x0380  | varies |
| DMAC_CH3_INTSTATUSUSO_REG                  | VDMA channel 3 interrupt status register                                   | 0x0388  | RO     |
| DMAC_CH3_INTSIGNAL_ENABLEO_REG             | VDMA channel 3 interrupt signal enable register                            | 0x0390  | varies |
| DMAC_CH3_INTCLEARO_REG                     | VDMA channel 3 interrupt clear register                                    | 0x0398  | WO     |
| DMAC_CH4_INTSTATUS_ENABLEO_REG             | VDMA channel 4 interrupt status enable register                            | 0x0480  | varies |
| DMAC_CH4_INTSTATUSUSO_REG                  | VDMA channel 4 interrupt status register                                   | 0x0488  | RO     |
| DMAC_CH4_INTSIGNAL_ENABLEO_REG             | VDMA channel 4 interrupt signal enable register                            | 0x0490  | varies |
| DMAC_CH4_INTCLEARO_REG                     | VDMA channel 4 interrupt clear register                                    | 0x0498  | WO     |
| status registers                           |                                                                             |         |        |
| DMAC_CH1_STATUSUSO_REG                     | VDMA channel 1 status register 0                                           | 0x0130  | RO     |
| DMAC_CH1_STATUSUS1_REG                     | VDMA channel 1 status register 1                                           | 0x0134  | RO     |
| DMAC_CH1_SSTATO_REG                        | VDMA channel 1 source status register                                      | 0x0160  | RO     |
| DMAC_CH1_DSTATO_REG                        | VDMA channel 1 destination status register                                 | 0x0168  | RO     |
| DMAC_CH1_SSTATARO_REG                      | VDMA channel 1 source status address register                               | 0x0170  | R/W    |
```