**Title:**
Chapter 22 Digital Signature (DS)

**Subtitles and Content with Descriptions of Registers:**

1. **Register 22.7, DS_QUERY_CHECK_REG (0x0E14)**
   - Description:
     ```
     DS_PADDING_BAD    : The padding check fails; O: The padding check passes. (RO)
     DS_MD_ERROR       : The MD check fails; O: The MD check passes. (RO)
     ```

2. **Register 22.8, DS_DATE_REG (0x0E20)**
   - Description:
     ```
     DS_DATE           Version control register. (R/W)
     ```

**Footer Information:**
- Company Name: Espressif Systems
- Document Title: ESP32-S3 TRM (Version 1.7)
- Page Number and Link to Submit Feedback: "907" and a link labeled "Submit Documentation Feedback"

**Diagram Description in the Image:**

There is no detailed diagram described, only references are made for specific bits within registers:
- For DS_QUERY_CHECK_REG register at bit positions (reserved), 31 through an unspecified number of lower bits.
- For DS_DATE_REG register also with a reference to "0x20191217" and the same range as above.

**Reset Indicators:**
- There are indications for reset in both registers, but no specific instructions on how or when they should be used.