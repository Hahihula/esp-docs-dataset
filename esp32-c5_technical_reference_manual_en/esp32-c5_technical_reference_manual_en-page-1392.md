

```markdown
Please refer to Section 38.5.1.2 CAN Frame Reception for programming procedures.

## 38.3.10 Fault Confinement

Fault confinement state of CAN FD is readable from TWAIFD_EWL_ERP_FAULT_STATE_REG register. Fault confinement state transition is displayed in Figure 38.3-14. Fault confinement counters are readable from REC and TEC registers. These counters correspond to the TX error counter and RX error counter as defined in ISO11898-1. CAN FD additionally contains counters distinguishing between errors detected in nominal bit rate and data bit rate. The nominal bit rate error counter (ERR_NORM) is readable from TWAIFD_ERR_NORM_VAL and it increments by 1 for each error detected at the nominal bit rate. The data bit rate error counter (ERR_FD) is readable from TWAIFD_ERR_FD_VAL and it increments by 1 due to each error detected at the data bit rate.

All four counters (REC, TEC, ERR_NORM, ERR_FD) can be manipulated by software. As this feature directly affects compliance of CAN FD to ISO11898-1, this is only allowed when TWAIFD_TSTM = 1 (in test mode). All counters can be set from software via TWAIFD_CTR_PRES_REG. Error warning limit (EWL) and error passive limit (ERP) are configured by TWAIFD_EWL and TWAIFD_ERP_LIMIT. By default, EWL and ERP comply with ISO11898-1. In the test mode, EWL and ERP fields are writable.

![Figure 38.3-14. Fault confinement](image)

## 38.3.11 Fault Tolerance

CAN FD implements following fault tolerance mechanisms:

* Parity protection on RX buffer RAM
* Parity protection on TX buffer RAM
* TX buffer backup mode (TWAIFD_TXBBM)

The following conditions must be met for these mechanisms to operate:

* Software drivers sets TWAIFD_PCHKE = 1. This field enables parity error detection. Software can modify TWAIFD_PCHKE only when TWAIFD_ENA = 0.

### 38.3.11.1 Parity Protection on RX Buffer RAM

When CAN FD receives a CAN frame and stores it to RX buffer RAM, it adds single parity bit to each word of RX buffer RAM. When software driver reads the frame from RX buffer RAM, it checks if a parity error occurs in the frame by reading TWAIFD_RXPE bit. CAN FD sets TWAIFD_RXPE upon each read from TWAIFD_RX_DATA, if the parity bit in the word being read from RX buffer RAM does not match the calculated parity bit.
```