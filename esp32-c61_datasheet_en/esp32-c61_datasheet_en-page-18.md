**Title: Pins**

---

### Table-2 - cont'd from previous page

| Pin No. | IO MUX / GPIO Name^1,2 | F0 | Type | F1 | I/O/T | F2 | Type |
|---------|------------------------|----|------|-----|-------|----|------|
| 7       | XTAL_32K_N             | GPIO1    | I/O   | GPIO1 | I/O/T | FSPIQ | I/O/T |
| 8       | GPIO2                  | GPIO2    | I/O   | GPIO2 | I/O/T | FSPIHD | I/O/T |
| 9       | MTMS                   | MTMS     | I      | GPIO3 | I/O    | FSPIWP | I/O/T |
| 10      | MTDI                   | MTDI     | I      | GPIO4 | I/O    |        |      |
| 11      | MTCK                   | MTCK     | I      | GPIO5 | I/O    |        |      |
| 12      | MTDO                   | MTDO     | I      | GPIO6 | O      | FSPICLK | I/O/T |
| 13      | SDIO_CMD               | SDIO_CMD | I/O   | GPIO25 | I/O    |        |      |
| 14      | SDIO_CLK               | SDIO_CLK | I/O   | GPIO26 | O      |        |      |
| 15      | SDIO_DATA0             | SDIO_DATA0 | I/O | GPIO27 | I/O    |        |      |
| 16      | SDIO_DATA1             | SDIO_DATA1 | I/O | GPIO28 | I/O    |        |      |
| 17      | SDIO_DATA2             | SDIO_DATA2 | I/O | GPIO29 | O      |        |      |
| 18      | SDIO_DATA3             | SDIO_DATA3 | I/O | GPIO30 | I/O    |        |      |
| 19      | SPICS1                 | SPICS1   | I/O   | GPIO14 | T      |        |      |
| 20      | SPICSQ                | SPICSQ   | O/T    | GPIO15 | I/O    |        |      |
| 22      | SPIQ                   | SPIQ     | I/O   | GPIO16 | I/O    |        |      |
| 23      | SPIWP                  | SPIWP    | I/O   | GPIO17 | O/T    |        |      |
| 24      | VDD_SPI               | VDD_SPI  | I/O   | GPIO18 | T      |        |      |
| 25      | SPIHD                 | SPIHD    | I/O   | GPIO19 | O/T    |        |      |
| 26      | SPICLK                | SPICLK   | O/T    | GPIO20 | I/O    |        |      |
| 27      | SPID                  | SPID     | I/O   | GPIO21 | T      |        |      |
| 28      | USB_D-                | USB_D-   | I/O   | GPIO12 | O/T    |        |      |
| 29      | USB_D+                | USB_D+   | I/O   | GPIO13 | O/T    |        |      |
| 30      | GPIO24                | GPIO24   | I/O   | GPIO24 | T      |        |      |
| 31      | GPIO8                 | GPIO8    | I/O   | GPIO8  | O/T    | FSPICSO | I/O/T |
| 32      | GPIO9                 | GPIO9    | I/O   | GPIO9  | O/T    |        |      |
| 33      | UORXD                 | UORXD    | I/O   | GPIO10 | T      |        |      |
| 34      | UOTXD                 | UOTXD    | O     | GPIO11 | I/O    |        |      |
| 35      | GPIO29                | GPIO29   | I/O   | GPIO29 | T      | FSPIID | I/O/T |
| 36      | GPIO7                 | GPIO7    | I/O   | GPIO7  | O/T    |        |      |

---

### Footnotes

1. Bold marks the default pin functions in the boot mode.
2. Regarding highlighted cells, see Section [2.4.3 Restrictions for GPIOs and LP GPIOs](#).
3. Each IO MUX function (Fn, n = 0 ~ 2) is associated with a type.

### Description of Type

- I – input
- O – output
- T – high impedance.
- If the pin is assigned to any other function than Fn, then:
  - The input signal of Fn always equals `1`.
  - The input signal of Fn always equals `0`.

---

**Source:**
Espressif Systems  
ESP32-C61 Series Datasheet v0.5

--- 

*Note: There is a watermark on the image that reads "PRIVACY POLICY" diagonally across it.*