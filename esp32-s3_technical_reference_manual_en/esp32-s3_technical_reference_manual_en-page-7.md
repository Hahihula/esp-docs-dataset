**Contents**

- **5 Overview**
  - [5.1](#section-51)
    - Features (410)

- **5 Functional Description**
  - Structure ([5.3.1](#section-531))
    - EFUSE_WR_DIS (417)
    - EFUSE_RD_DIS (417)
  - Data Storage ([5.3.2](#section-532))
    - Programming of Parameters (418)
  - User Read of Parameters ([5.3.3](#section-533))
  - eFuse VDDQ Timing ([5.3.4](#section-534))
  - The Use of Parameters by Hardware Modules ([5.3.5](#section-535))
  - Interrupts ([5.3.6](#section-536))
  - Register Summary ([5.4](#section-54))
    - Registers (427)

**III System Component**

- **6 IO MUX and GPIO Matrix (GPIO, IO MUX)**
  - Overview ([6.1](#section-61))
    - Features (472)
  - Architectural Overview ([6.3](#section-63))
    - Peripheral Input via GPIO Matrix
      - [6.4.1](#section-641)
        - Overview (474)
      - Signal Synchronization ([6.4.2](#section-642))
      - Functional Description ([6.4.3](#section-643))
      - Simple GPIO Input ([6.4.4](#section-644))
    - Peripheral Output via GPIO Matrix
      - [6.5](#section-65)
        - Overview (476)
      - Functional Description ([6.5.2](#section-652))
      - Simple GPIO Output ([6.5.3](#section-653))
      - Sigma Delta Modulated Output ([6.5.4](#section-654))
        - [6.5.4.1](#section-6541)
          - Functional Description (478)
        - SDM Configuration ([6.5.4.2](#section-6542))
      - Direct Input and Output via IO MUX
        - Overview ([6.6](#section-66))
        - Functional Description ([6.6.2](#section-662))
    - RTC IO MUX for Low Power and Analog Input/Output ([6.7](#section-67))
      - [6.7.1](#section-671)
        - Overview (479)
      - Low Power Capabilities ([6.7.2](#section-672))
      - Analog Functions ([6.7.3](#section-673))
    - Pin Functions in Light-sleep
      - [6.8](#section-68)
        - Pin Hold Feature (480)
    - Power Supply and Management of GPIO Pins
      - [6.10](#section-610)
        - Power Supply of GPIO Pins ([6.10.1](#section-6101))
        - Power Supply Management ([6.10.2](#section-6102))
    - Peripheral Signals via GPIO Matrix ([6.11](#section-611))

**Footer**
- Espresso Systems
- Submit Documentation Feedback

**Page Information:**
- ESP32-S3 TRM (Version 1.7)
- Page number: 7