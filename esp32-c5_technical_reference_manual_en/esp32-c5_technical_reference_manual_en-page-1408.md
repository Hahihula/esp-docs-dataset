

```markdown
Register 38.4. TWAIFD_INT_STAT_REG (0x0010)

| Bit | Name                     | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  |                          | (reserved)                                                                  |
| 30-0|                          | TWAIFD_TXBHCI_INT_ST, TWAIFD_RBNEI_INT_ST, TWAIFD_RXFI_INT_ST, ...         |

TWAIFD_RXI_INT_ST   The masked interrupt status of TWAIFD_RXI_INT. (R/W1C)
TWAIFD_TXI_INT_ST   The masked interrupt status of TWAIFD_TXI_INT. (R/W1C)
TWAIFD_EWLI_INT_ST  The masked interrupt status of TWAIFD_EWLI_INT. (R/W1C)
TWAIFD_DOI_INT_ST   The masked interrupt status of TWAIFD_DOI_INT. (R/W1C)
TWAIFD_FCSI_INT_ST  The masked interrupt status of TWAIFD_FCSI_INT. (R/W1C)
TWAIFD_ALI_INT_ST   The masked interrupt status of TWAIFD_ALI_INT. (R/W1C)
TWAIFD_BEI_INT_ST   The masked interrupt status of TWAIFD_BEI_INT. (R/W1C)
TWAIFD_OFI_INT_ST   The masked interrupt status of TWAIFD_OFI_INT. (R/W1C)
TWAIFD_RXFI_INT_ST  The masked interrupt status of TWAIFD_RXFI_INT. (R/W1C)
TWAIFD_BSI_INT_ST   The masked interrupt status of TWAIFD_BSI_INT. (R/W1C)
TWAIFD_RBNEI_INT_ST The masked interrupt status of TWAIFD_RBNEI_INT. (R/W1C)
TWAIFD_TXBHCI_INT_ST The masked interrupt status of TWAIFD_TXBHCI_INT. (R/W1C)
```