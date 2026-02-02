**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Register Information:**
- Register Name: EMACFF_REG (0x1004)
- Bit Fields:
  - RECEIVE_ALL (bit positions reserved, bit values from left to right): 31...0
    - Description for RECEIVE_ALL when set and not set.
      - When this bit is set (`RECEIVE_ALL = 1`), the MAC Receiver module passes all received frames irrespective of whether they pass the address filter or not. The result updates (pass or fail) in corresponding bits in the Receive Status Word, with reset condition for receiving only those to application passing SA or DA address filter.
      - When this bit is clear (`RECEIVE_ALL = 0`), MAC compares received frames' SA field values against enabled SA registers; if not a match, frame dropped. The Rx Status updates based on the comparison.

  - SAFE (bit positions reserved): 
    - When set: MAC forwards all control frames to application even failing Address Filter.
    - When clear (`SAFE = 0`), MAC drops received frames that fail address filter check against SA registers; Rx Status updated accordingly for each frame's SA match or mismatch with registered addresses.

  - SAIF (bit positions reserved):
    - When set: Address Check block operates in inverse filtering mode, marking SA matches as failing.
    - When clear (`SAIF = 0`), frames not matching SA registers are marked successful; Rx Status updates accordingly for each frame's address comparison success or failure with registered addresses.

  - PCF (bit positions reserved):
    - Controls forwarding of all control and multicast Pause frames, including conditions:
      - `2'b00`: MAC filters out application-bound control/PAUSE frames.
      - `2'b01`: MAC forwards except PAUSE to app even if fail Address filter check; Rx Status updates accordingly for each frame's address comparison success or failure with registered addresses.

  - DBF (bit positions reserved):
    - When set: AFM module blocks all incoming broadcast and multicast control/PAUSE frames, overriding other filters.
    - When clear (`DBF = 0`), the AFM passes received broadcast frames; Rx Status updates accordingly for each frame's address comparison success or failure with registered addresses.

  - PAM (bit positions reserved):
    - Indicates that all incoming broadcasts with multicast destination pass through if first bit in destination field is '1'; Rx Status updated based on this condition being met by the packet’s destination addressing criteria. 

**Additional Information:**
- Conditions for Pause frames processing:
  - Condition 1 and 2 specify conditions related to MAC address settings.
  - Condition 3 specifies type fields of received frame.

**Footer Note:** 
Continued information is available in subsequent pages, specifically on page `503` under ESP32 TRM (Version 5.6).