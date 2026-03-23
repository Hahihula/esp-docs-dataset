

```markdown\n| Mode          | Sub-mode                | Description                                                                 |\n|---------------|-------------------------|-----------------------------------------------------------------------------|\n| LEVEL_ENABLE  | sub-mode 1              | signal level high                                                           |\n|               |                         | Valid data →                                                               |\n|               | sub-mode 2              | signal level low                                                            |\n|               |                         | Valid data →                                                               |\n```
Figure 38.5-4. Sub-Modes of Level Enable Mode for RX Unit

### 38.5.4.2 Pulse Enable Mode

Pulse Enable mode can be divided into 12 sub-modes depending on the pulse active level and its alignment with valid data. For detailed classification, see Figure 38.5-5.

Sub-modes 1 ~ 8 all contain start pulse and end pulse. The difference lies in whether start pulse and end pulse are aligned with valid data.

Sub-modes 9 ~ 12 only contain start pulse and the end of valid data is signaled by configuring `PARL_IO_RX_DATA_BYTELEN`.

Since the external pulse enable signal occupies one IO pin, there are at most 15 IO pins left usable for RXD. However, in sub-modes 4, 8, 10, and 12, as the data is considered valid before the pulse’s first edge and after the pulse’s last edge, the enable signal IO pin can serve as a data IO pin at the same time. Therefore, there are 16 IO pins usable for RXD in these sub-modes.
```