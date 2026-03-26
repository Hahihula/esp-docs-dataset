

```markdown
Chapter 34 Key Manager

- Deploy the negotiated private key using the auxiliary key
- No need to boot the chip to obtain the private key
• Random key deployment (Random Deploy Mode):
  - Deploys a hardware-generated random key with nobody knowing the exact value
• Private key recovery deployment (Private Key Recovery Mode):
  - Recovers exactly the same key by entering the key information generated during deployment
• Key information export (key_info Export Mode):
  - Generates unique key information for the same key each time

34.5 Architectural Overview

The top-level architecture of the Key Manager and HUK Generator is shown in the figure below.

Figure 34.5-1. Architecture of Key Manager and HUK Generator

The Key Manager has the following interaction paths with external modules:
• eFuse path: Controls the configuration of Key Manager with the help of eFuse bits.
• HP APB path: Configures registers and transmits memory data via HP APB bus.
• HUK path: Receives HUK from HUK Generator.
• Crypto path: Controls cryptographic accelerators such as ECC/AES to complete cryptographic operations via Crypto APB bus.
• TRNG path: Receives true random data from the TRNG.
```