
```markdown
Chapter 31 Key Manager

The HUK Generator has the following interaction paths with external modules.

*   eFuse path: Controls the configuration of HUK Generator with the help of eFuse bits.
*   LP APB path: Configures registers and transmits memory data via LP APB bus.
*   Key Manager path: Sends HUK to Key Manager.

31.6 Functional Description

31.6.1 HUK Generator

HUK Generator generates unique HUKs for each chip based on SRAM Physical Unclonable Function (PUF). This HUK is completely inaccessible by software, ensuring robust security for the Key Manager, which relies on this HUK for secure operations later on.

31.6.1.1 HUK Generation Process

The HUK Generator has the following modes:

*   **HUK Generation Mode:** Creates a new HUK and generates corresponding HUK recovery information (`huk_info`).
*   **HUK Recovery Mode:** Recovers HUK according to `huk_info`.

The modes above are jointly controlled by the eFuse EFUSE_KM_HUK_GEN_STATE and the register `HUK_MODE`, as shown in the following table.

Table 31.6-1. HUK Generator Working Mode

| HUK_MODE | eFuse * | Mode |
|----------|---------|-------|
| 1        | Total number of bits set to 1 is even | HUK Generation Mode |
|          | Total number of bits set to 1 is odd   | HUK Recovery Mode |
| 0        | —                             | HUK Recovery Mode |

*   Total number of bits set to 1 in EFUSE_KM_HUK_GEN_STATE.

Note:

*   Once the process is completed in HUK Generation Mode, it is recommended to write a 1 to EFUSE_KM_HUK_GEN_STATE, ensuring that the total number of bits set to 1 in EFUSE_KM_HUK_GEN_STATE is an odd number. With this, when the chip starts next time, the HUK Generator can only enter HUK Recovery Mode. The HUK restored in HUK Recovery Mode will be the same as the one generated this time in HUK Generation Mode.
*   If you do not update the eFuse EFUSE_KM_HUK_GEN_STATE after completing the HUK Generation Mode and before powering off the chip, the HUK Generator can still be configured to enter HUK Generation Mode again when the chip is powered on next time. The newly generated HUK this time will have a different value from the previous one that is used in private keys. By this way, you can generate multiple HUKs and restore the one you need with its `huk_info`.
*   `huk_info` can only be used with the same chip; that is, an `huk_info` generated on chip A can not be used to recover the HUK on chip B.
```