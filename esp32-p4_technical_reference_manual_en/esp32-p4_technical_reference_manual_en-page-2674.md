

```markdown
Register 52.50. EMACTSTPCTRL_REG (0x0700)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

TSENMACADDR Configures whether to enable the DA MAC address (that matches any MAC Address register) for PTP frame filtering when PTP is directly sent over Ethernet.
O: Disable
1: Enable
(R/W)

SNAPTYPSSEL Configures the set of PTP packet types for which snapshot needs to be taken, in combination with TSMSTRENA and TSEVNTENA.

SNAPTYPSSEL, TSMSTRENA, TSEVNTENA:
00x0: SYNC, Follow_Up, Delay_Req, Delay_Resp
0001: SYNC
0011: Delay_Req
01x0: SYNC, Follow_Up, Delay_Req, Delay_Resp, Pdelay_Req, Pdelay_Resp, Pdelay_Resp_Follow_Up
0101: SYNC, Pdelay_Req, Pdelay_Resp
0111: Delay_Req, Pdelay_Req, Pdelay_Resp
10xx: SYNC, Delay_Req
11xx: Pdelay_Req, Pdelay_Resp
(R/W)

TSMSTRENA Configures whether to enable snapshot only for messages relevant to the master node.
O: Disable. The snapshot is taken for the messages relevant to the slave node
1: Enable
(R/W)

TSEVNTENA Configures whether to enable timestamp snapshot only for event messages (SYNC, Delay_Req, Pdelay_Req, Pdelay_Resp).
O: Disable. The snapshot is taken for all messages except Announce, Management, and Signaling
1: Enable
(R/W)

TSIPV4ENA Configures whether to enable the processing of PTP frames sent over IPv4-UDP.
O: Disable. The MAC ignores the PTP transported over UDP-IPv4 packets
1: Enable. The MAC receiver processes the PTP packets encapsulated in UDP over IPv4 packets
(R/W)

Continued on the next page...
```