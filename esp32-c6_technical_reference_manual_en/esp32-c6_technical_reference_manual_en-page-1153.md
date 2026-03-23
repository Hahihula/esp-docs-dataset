

```markdown
## 34.9.3 SLC Host Registers

Register 34.40. SLCHOST_CONF_REG (0x01F0)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 28-27     | (reserved)                                                                  |
| 26        | SLCHOST_HSPEED_CON_EN                                                       |
| 20-19     | (reserved)                                                                  |
| 15-14     | SLCHOST_FRC_POS_SAMP                                                        |
| 10-9      | SLCHOST_FRC_NEG_SAMP                                                        |
| 5-4       | SLCHOST_FRC_SDIO20                                                          |
| 0         | SLCHOST_FRC_SDIO11                                                          |

<table>
<thead>
<tr>
<th>Reset</th><th>31</th><th>30</th><th>29</th><th>28</th><th>27</th><th>26</th><th>25</th><th>24</th><th>23</th><th>22</th><th>21</th><th>20</th><th>19</th><th>18</th><th>17</th><th>16</th><th>15</th><th>14</th><th>13</th><th>12</th><th>11</th><th>10</th><th>9</th><th>8</th><th>7</th><th>6</th><th>5</th><th>4</th><th>3</th><th>2</th><th>1</th><th>0</th>
</tr>
</thead>
<tbody>
<tr>
<td></td><td>OxO</td><td></td><td></td><td></td><td></td><td>0</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td>OxO</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td>OxO</td>
</tr>
</tbody>
</table>

SLCHOST_FRC_SDIO11 Configure 1 to bit[4] to force drive CMD signal at the falling clock edge. Configures 1 to bit[3:0] corresponding bit to force drive DAT[3:0] signal corresponding bit at the falling clock edge. (R/W)

SLCHOST_FRC_SDIO20 Configure 1 to bit[4] to force drive CMD signal at the rising clock edge. Configures 1 to bit[3:0] corresponding bit to force drive DAT[3:0] signal corresponding bit at the rising clock edge. (R/W)

SLCHOST_FRC_NEG_SAMP Configure 1 to bit[4] to force sample CMD signal at the falling clock edge. Configures 1 to bit[3:0] corresponding bit to force sample DAT[3:0] signal corresponding bit at the falling clock edge. (R/W)

SLCHOST_FRC_POS_SAMP Configure 1 to bit[4] to force sample CMD signal at the rising clock edge. Configures 1 to bit[3:0] corresponding bit to force sample DAT[3:0] signal corresponding bit at the rising clock edge. (R/W)

SLCHOST_HSPEED_CON_EN Configures 1 to this bit, configures 1 to HINF_HIGHSPEED_ENABLE, and then the host configures 1 to EHS in CCCR to force drive CMD and DAT signals at the rising clock edge. (R/W)
```