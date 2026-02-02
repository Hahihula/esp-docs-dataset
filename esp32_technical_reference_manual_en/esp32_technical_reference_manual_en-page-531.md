**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**GoBack Link:** GoBack

**Section Heading and Subheading with Content:**

- **Subsection Header**: A maximum of two Overload frames may be generated in order to delay the next Data or Remote Frame.
  
- **Subsection Title**: 25.3.2.3 Interframe Space
  - The text explains that an Interframe Space acts as a separator between frames, and it details how data is separated from preceding frames by this space.

**Figure Description:**
- Figure Caption:** Figure 25.3-4 shows the fields within an Interframe Space:
  
**Table Title**: Table 25.3-4. Interframe Space
- **Table Content:**
  - Column Headers: Interframe Space, Description.
  - Rows:
    - Row for "Intermission (3 bits)": The text describes that this consists of three recessive bits and is related to an error passive node just transmitting a message which must include the Suspend Transmission field. This should not be included in Error Active nodes' fields.

**Subsection Title**: 25.3.3 TWAI Errors

- **Subsection Subtitle:** 25.3.3.1 Error Types
  - The text categorizes bus errors into different types:
    - Bit Error: Describes what happens when a bit value is transmitted but the opposite (Dominant or Recessive) bit detected.
    - Stuff Error: Occurs if six consecutive bits of the same type are received, violating stuffing encoding rules.
    - CRC Error: A receiver calculates a CRC based on incoming data and checks it against the calculated sequence in Data/Remote Frame.

**Footer Information:** 
- Page Number 531
- Document Title ESP32 TRM (Version 5.6)
- Link to Submit Documentation Feedback