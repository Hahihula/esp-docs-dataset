

```markdown
## 40.5 Functional Description

This section introduces the operating states and modes of the MIPI RX D-PHY and the major functions that facilitate the use of MIPI CSI. For detailed configurations, refer to Section 40.7 Programming Procedures.

### 40.5.1 Data Lane State

The functions of the transmitter determine the data lane state by driving certain line levels. During normal operation, either an HS-TX or an LP-TX is driving a lane.

*   **HS-TX:** High-Speed transaction. An HS-TX always drives the lane differentially. It operates in two states: HS-O and HS-1. When HS-TX drives the lane, the lane remains in High-Speed Data Reception mode.
    *   - HS-O: Transmits differential data 0 in High-Speed Data Reception mode.
    *   - HS-1: Transmits differential data 1 in High-Speed Data Reception mode.

*   **LP-TX:** Low-Power transaction. The two LP-TXs drive the two lines of a lane independently and single-ended. It operates in four states: LP-00, LP-01, LP-10, and LP-11. When LP-TX drives the lane, the lane is in Control mode or Escape mode.
    *   - LP-00: A bridge state between other LP states (LP-01, LP-10, LP-11) in Control Mode or Escape Mode. When in Ultra Low Power State (ULPS), lanes are also in the LP-00 state.
    *   - LP-01: Transmits data 0 in Escape mode, or indicates entry into High-Speed Data Reception mode from Control mode.
        The complete sequence for entering High-Speed Data Reception mode is: LP-11 → LP-01 → LP-00
    *   - LP-10: Transmits data 1 in Escape mode, or indicates entry into Escape mode or Turnaround mode from Control mode.
        The complete sequence for entering Escape mode is: LP-11 → LP-10 → LP-00 → LP-01 → LP-00.
        The complete sequence for entering the Turnaround mode is: LP-11 → LP-10 → LP-00 → LP-10 → LP-00
    *   - LP-11: The stop state, i.e., the default idle state of a lane.

**Note:**
The Turnaround mode is used for switching the data transmission direction. This mode is not used in the ESP32-P4 MIPI CSI, and will not be further explained in this chapter.
```

Figure 40.5-1 shows the lane line levels for High-Speed (HS) and Low-Power (LP) transactions.
```