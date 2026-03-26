

```markdown
Chapter 20 System Registers (SYSREG)

GoBack

20.2.1.15 AXI Matrix

ESP32-P4's AXI Matrix connects multiple AXI-compliant master and slave devices, enabling efficient communication.

*   Masters such as all AHB masters (master port1 through AHB2AXI bridge), HP CPU cache (master port2), DW GDMA_0 (master port6), DW GDMA_1 (master port7), AXI GDMA (master port9), 2DDMA (master port11), H264_0 (master port12), and H264_1 (master port13)
*   Slaves such as L2MEM (slave port2), Flash (slave port3), PSRAM (slave port4), DSI Host (slave port6) and CSI Host(slave port7).

All AXI master ports except master port 2 in the AXI matrix support the QoS (Quality of Service) bandwidth regulator. The AXI matrix also includes a deadlock timeout protection mechanism, slave arbiter priority configuration for slave ports, and QoS arbiter priority configuration for master ports.

Deadlock Timeout Protection

ESP32-P4's Deadlock Timeout Protection is always enabled. Configure the timeout threshold for all AXI masters in the AXI matrix that access AXI Slaves such as Flash, PSRAM, DSI HOST, and CSI HOST via HP_SYSTEM_ICM_DLOCK_TIMEOUT_REG.

When a timeout occurs, AXI Matrix will record transfer direction, AXI ID, master ID and slave ID in HP_SYSTEM_ICM_DLOCK_STATUS_REG, and assert ICM_DLOCK_INTR interrupt at the same time.

Slave Arbiter Priority

Configure the arbitration priority for slaves in the AXI Matrix to arbitrate reading data and responses via HP_SYSTEM_ICM_SLV_ARB_PRIORITY_REG.

The higher the value, the higher the priority.

Master QoS Arbiter Priority

Configure the QoS (Quality of Service) values for masters in the AXI matrix to arbitrate the read address channel and write address channel via HP_SYSTEM_ICM_MST_ARQOS_REG0_REG and HP_SYSTEM_ICM_MST_AWQOS_REG0_REG, respectively.

A higher QoS value indicates a higher priority during arbitration.

20.2.1.16 Post Write

The following registers controls the Post Write mode of different components to speed up the write access.

*   `HP_SYSTEM_PERI1_APB_POSTW_EN_REG`: enables the Post Write mode for APB2APB bridge between peripherals.
*   `HP_SYSTEM_APB_SYNC_POSTW_EN_REG`: enables the Post Write mode for APB2APB bridge in DSI, CSI and ISP.
*   `HP_SYSTEM_CPU_ICM_H2X_POST_WR_EN`: enables the Post Write mode for AHB2AXI bridge from AHB masters to AXI slaves.

Espressif Systems
1245
ESP32-P4 TRM
Submit Documentation Feedback PRELIMINARY
```