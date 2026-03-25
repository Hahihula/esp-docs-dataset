

```markdown
Chapter 3  GDMA Controller (GDMA)

GoBack

The last descriptor of linked list

Next descriptor address

Next descriptor address

New linked list

Figure 3.4-2. Relationship among Linked Lists

3.4.5 Linked List Reading Process

Once configured and enabled by software, the GDMA controller starts to read the linked list from internal RAM.
The GDMA performs checks on descriptors in the linked list. Only if descriptors pass the checks, the
corresponding GDMA channel will start data transfer. If the descriptors fail any of the checks, hardware will
trigger a descriptor error interrupt (either GDMA_IN_DSCR_ERR_CHn_INT or
GDMA_OUT_DSCR_ERR_CHn_INT), and the channel will halt.

The checks performed on descriptors are:

- Owner bit check when GDMA_IN_CHECK_OWNER_CHn or GDMA_OUT_CHECK_OWNER_CHn is set to 1.
If the owner bit is 0, the buffer is accessed by the CPU. In this case, the owner bit fails the check. The
owner bit will not be checked if GDMA_IN_CHECK_OWNER_CHn or GDMA_OUT_CHECK_OWNER_CHn is
0.

- Buffer address pointer (DW1) check. If the buffer address pointer points to 0x40800000 ~ 0x4084FFFF
(please refer to Section 3.4.7), it passes the check. Otherwise, it fails the check.

After software detects a descriptor error interrupt, it must reset the corresponding channel, and enable GDMA
by setting GDMA_OUTLINK_START_CHn or GDMA_INLINK_START_CHn bit.

Note: The third word (DW2) in a descriptor can only point to a location in internal RAM, given that the third
word points to the next descriptor to use and that all descriptors must be in internal memory.

3.4.6 EOF

The GDMA controller uses EOF (end of frame) flags to indicate the end of data segment transfer
corresponding to a specific descriptor.

Before the GDMA controller transmits data, the GDMA_OUT_TOTAL_EOF_CHn_INT_ENA bit should be set to
enable the GDMA_OUT_TOTAL_EOF_CHn_INT interrupt. If data in the buffer pointed by the last descriptor
(with EOF) has been transmitted, a GDMA_OUT_TOTAL_EOF_CHn_INT interrupt is generated.

Before the GDMA controller receives data, the GDMA_IN_SUC_EOF_CHn_INT_ENA bit should be set to enable
the GDMA_IN_SUC_EOF_CHn_INT interrupt. If a data segment with an EOF flag has been received
successfully, a GDMA_IN_SUC_EOF_CHn_INT interrupt is generated. In addition, when the GDMA channel is

Espressif Systems
108
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```