Title: ESP32-C6 Series Comparison

Subtitle: Nomenclature (1.1)

Diagram:
- The diagram shows a block labeled "ESP32-C6" with three arrows pointing to the right, each leading into different labels.
  - First arrow points towards an icon representing flash size in megabytes and is accompanied by text that reads “Flash size (MB)”
  - Second arrow indicates temperature conditions for high-temperature environments ("H: High temperature") or normal temperatures ("N: Normal temperature").
  - Third arrow leads to a label "In-package flash".
  - Fourth arrow points towards the chip series.

Caption under diagram:
- Figure caption reads “Figure 1.1- ESP32-C6 Series Nomenclature”

Subtitle: Comparison (1.2)

Table Title: Table 1-1. ESP32-C6 Series Comparison

Table Content:

| Part Number | In-Package Flash | Ambient Temp. | Package                | Chip Revision |
|-------------|------------------|---------------|------------------------|--------------|
| ESP32-C6    | -3               | -40 ~ 105 °C | QFN40 (5×5 mm)        | v0.0/v0.1/v0.2|
| ESP32-C6FH4 | Quad SPI       | 4 MB         | QFN32 (5×5 mm)        | v0.0/v0.1/v0.2|
| ESP32-C6FH8 | Quad SPI       | 8 MB         | QFN32 (5×5 mm)        | v0.0/v0.1/v0.2|

Table Footnotes:
- Note for Part Number: "For details on chip marking and packing, see Section 7 Packaging."
- Note for In-Package Flash: "Ambient temperature specifies the recommended temperature range of the environment immediately outside an Espressif chip.”
- Note for Ambient Temp.: "Can connect a flash outside the chip package. For details, see Section 4.1.2.2 External Memory"
- Note for Package and Chip Revision:
  - “For information about SPI modes, see Section 2.6 Pin Mapping Between Chip and Flash."
  - “For more info about in-package flash, also refer to Section 4.1.2.1 Internal Memory.”
  - "By default, the SPI flash on the chip operates at a maximum clock frequency of 80 MHz and does not support auto suspend feature."

Subtitle: Chip Revision (1.3)

Body Text:
- As shown in Table 1-1 ESP32-C6 Series Comparison, ESP32-C6 now has multiple chip revisions available on the market using the same part number.
- For chip revision identification, ESP-IDF release that supports a specific chip revision and errors fixed in each chip revision refer to ESP32-C6 Series SoC Errata.

Footer:
- "Espressif Systems"
- Page Number: 13
- Link Text for Feedback Submission: “Submit Documentation Feedback”