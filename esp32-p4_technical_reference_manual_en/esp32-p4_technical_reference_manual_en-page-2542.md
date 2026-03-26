

```markdown
USB_GINTSTS_REG

31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17:10 | 9 | 8 | 7:3 | 2 | 1 | 0
----------------------------------------------------------------------------------------------------
USB_GINTMSK_REG

Interrupt Sources

USB_HPRT_REG
USB_HAINT_REG
JSB_HCINTn_REG (0-15)

USB_DAIMTMSK_REG
USB_DAINT_REG
OUT EP | IN EP
31:16 | 15:0

GOTGINT Register

OR
AND

Interrupt Signal

USB_GBLINTRMSK

Figure 49.4-5. OTG_HS Interrupt Hierarchy


The following bits of the USB_GINTSTS_REG register indicate an interrupt source lower in the hierarchy:

*   **USB_PRTINT** indicates that the Host port has a pending interrupt. The USB_HPRT_REG register indicates the interrupt source.
*   **USB_HCHINT** indicates that one or more Host channels have a pending interrupt. Read the USB_HAINT_REG register to determine which channel(s) have a pending interrupt, then read the pending channel's USB_HCINTn_REG register to determine the interrupt source.
*   **USB_OEPINT** indicates that one or more OUT endpoints have a pending interrupt. Read the USB_DAINT_REG register to determine which OUT endpoint(s) have a pending interrupt, then read the USB_DOEPINTn_REG register to determine the interrupt source.
*   **USB_IEPINT** indicates that one or more IN endpoints have a pending interrupt. Read the USB_DAINT_REG register to determine which IN endpoint(s) are pending, then read the pending IN endpoint's USB_DIEPINTn_REG register to determine the interrupt source.
*   **USB_OTGINT** indicates an On-The-Go event has triggered an interrupt. Read the USB_GOTGINT_REG register to determine which OTG event(s) triggered the interrupt.
```