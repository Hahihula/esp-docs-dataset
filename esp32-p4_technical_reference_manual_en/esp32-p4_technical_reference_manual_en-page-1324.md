

```markdown
Register 20.105. LP_SYSTEM_LP_ADDRHOLE_INFO_REG (0x016C)
```

```plaintext
31
+-----------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
+-----------------------------------------------------------------------------+
| Reset                                                LP_SYSTEM_LP_ADDRHOLE_SECURE
|                                                     LP_SYSTEM_LP_ADDRHOLE_WR
|                                                     LP_SYSTEM_LP_ADDRHOLE_ID
|
| (reserved)
```

LP_SYSTEM_LP_ADDRHOLE_ID Represents the master ID when LP_ADDRHOLE_INT occurs.

O: LP CPU0  
1: LP CPU1  
2: LP CPU  
3: USB OTG11  
4: Reserved  
5: GMAC  
6: SDMMC  
7: USBOTG20  
8: TRACEO  
9: TRACE1  
10: SPM monitor  
11: L2MEM monitor  
16~31: AHB PDMA (RO)

LP_SYSTEM_LP_ADDRHOLE_WR Represents the direction of transfer when LP_ADDRHOLE_INT occurs.

1: Write transfer  
0: Read transfer (RO)

LP_SYSTEM_LP_ADDRHOLE_SECURE Represents the address hole type when LP_ADDRHOLE_INT occurs.

1: Illegal address access  
0: Access without permission (RO)
```