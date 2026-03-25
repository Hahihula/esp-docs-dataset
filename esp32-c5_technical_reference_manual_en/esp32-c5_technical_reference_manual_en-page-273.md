

```markdown
Chapter 7 eFuse Controller (EFUSE)                                                                 GoBack

Register 7.5. EFUSE_RD_REPEAT_DATA1_REG (0x0034)

Continued from the previous page...

EFUSE_KM_DEPLOY_ONLY_ONCE Represents whether the corresponding key can be deployed only once.
Bit0: Represents whether the ECDSA key can be deployed only once
O: The key can be deployed multiple times
1: The key can be deployed only once
Bit1: Represents whether the XTS-AES (flash and PSRAM) key can be deployed only once
O: The key can be deployed multiple times
1: The key can be deployed only once
Bit2: Represents whether the HMAC key can be deployed only once
O: The key can be deployed multiple times
1: The key can be deployed only once
Bit3: Represents whether the DS key can be deployed only once
O: The key can be deployed multiple times
1: The key can be deployed only once
(RO)

EFUSE_FORCE_USE_KEY_MANAGER_KEY Represents whether the corresponding key must come from Key Manager.
Bit0: Represents whether the ECDSA key must come from Key Manager.
O: The key does not need to come from Key Manager
1: The key must come from Key Manager
Bit1: Represents whether the XTS-AES (flash and PSRAM) key must come from Key Manager.
O: The key does not need to come from Key Manager
1: The key must come from Key Manager
Bit2: Represents whether the HMAC key must come from Key Manager.
O: The key does not need to come from Key Manager
1: The key must come from Key Manager
Bit3: Represents whether the DS key must come from Key Manager.
O: The key does not need to come from Key Manager
1: The key must come from Key Manager
(RO)

EFUSE_FORCE_DISABLE_SW_INIT_KEY Represents whether to disable the use of the initialization key written by software and instead force use efuse_init_key.
O: Enable
1: Disable
(RO)

Continued on the next page...
```