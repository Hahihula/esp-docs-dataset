

```markdown
- Deploy the negotiated private key using the auxiliary key
- No need to boot the chip to obtain the private key

• Random key deployment (Random Deploy Mode):
  - Deploys a hardware-generated random key with nobody knowing the exact value

• Private key recovery deployment (Private Key Recovery Mode):
  - Recovers exactly the same key by entering the key information generated during deployment

• Key information export (key_info Export Mode):
  - Generates unique key information for the same key each time
```

## 31.5 Architectural Overview

The top-level architecture of the Key Manager and HUK Generator is shown in the figure below.

![Figure 31.5-1. Architecture of Key Manager and HUK Generator](image_description_not_provided)

### Description:

**Components:**

- **LP CPU**: Connected via `apb_bus` to HUK Data Memory.
- **HUK Data Memory**: Stores raw data from PUF SRAM for fuzzy extraction.
- **PUF SRAM**: Provides `raw_data` to Fuzzy Extraction; connected internally within the HUK Generator block (highlighted in red).
- **Fuzzy Extraction**: Processes `raw_data` into `fuzzy_data`.
- **RS encoder/decoder**: Takes `fuzzy_data` as input and outputs processed data toward HP CPU/MSPi.
- **HUK Generator**:
  - Receives signals like `huk_gen_state`, `deploy_once`, `init_key`, etc., from eFuse.
  - Outputs `huk` (Hardware Unique Key) with validity signal `huk_valid`.
- **Access Control**, **Key Generator**: Part of the main Key Manager block receiving HUK and managing keys.
- **Key Manager Data Memory**: Stores key-related data accessible via APB bus to HP CPU/Crypto_Perl.
- **Crypto_Perl**: Receives crypto keys over APB bus from Key Manager for cryptographic operations.
- **TRNG**: Supplies `md_num` (likely seed or identifier) and random data (`huk_gen_state`, etc.) to eFuse path; connected via internal signals.
- **eFuse**: Manages configuration bits for key manager initialization.
- **HP CPU** & **MSPi**: High-performance interfaces handling secure communication with Key Manager.

### Interaction Paths:

- **eFuse path**: Controls the configuration of Key Manager using eFuse bits.
- **HP APB path**: Configures registers and transmits memory data via HP APB bus.
- **HUK path**: Receives HUK from HUK Generator.
- **Crypto path**: Controls cryptographic accelerators (ECC/AES) over Crypto APB bus.
- **TRNG path**: Receives true random data from TRNG.

---

Espressif Systems  
990  
ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```