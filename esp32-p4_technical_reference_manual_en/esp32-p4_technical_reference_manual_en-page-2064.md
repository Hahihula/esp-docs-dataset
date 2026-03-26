

```markdown
INITIALIZATION

Shut-Down
No-Power

AFE Initialization

ACTIVE STATE

Control Mode

Escape Mode
Ultra Low-Power State

High-Speed Mode

Figure 40.5-2. MIPI RX D-PHY Operating States and Modes
```

### 40.5.2.1 No-Power State

In the No-Power state, no supply voltage is applied to the PHY.

The MIPI RX D-PHY of MIPI CSI is in No-Power state when the power supply VDD_HP_n (n: 0-3) and VDD_MIPI_DPHY are off.

### 40.5.2.2 Shut-Down State

Shut-Down state refers to the idle state.

In Shut-Down state, the PHY disables all analog blocks, resets all digital logic, and sets the DOP/DON, D1P/D1N, and CP/CN lanes to high impedance (Hi-Z). Activating the Shut-Down state ensures the lowest power consumption. To enable the Shut-Down state of the PHY, set `CSI_HOST_DPHY_RSTZ` and `CSI_HOST_PHY_SHUTDOWNZ` to 0.

Before leaving the Shut-Down state, configure several parameters, including the lane number to be used and the lane operation frequency range.

The MIPI RX D-PHY consists of two data lanes. Configure `CSI_HOST_N_LANES` to select either one or both data lanes. These configurations should remain static or stable before exiting the Shut-Down state.

Depending on the specific requirements for the MIPI RX D-PHY, additional configuration steps might be necessary. By default, the PHY operates within a lower range of 80-110 Mbps. To accommodate higher bit rates, adjust the HS frequency ranges (the hsfreqrange field) in test code `HS RX Control of lane 0` with the appropriate code. It is recommended to perform this adjustment in the Shut-Down state, as the control interface is independent of the reset of the MIPI RX D-PHY.
```