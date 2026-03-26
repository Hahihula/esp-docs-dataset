

```markdown
Chapter 31 ECDSA Digital Signature Peripheral (ECDSA_DS) GoBack


Among them, the SHA accelerator will be released when `ECDSA_SHA_RELEASE_INT` is triggered, while the ECC accelerator will be occupied during the whole ECDSA_DS operation.

Note:
Hardware occupation is a mechanism to protect multiplexed modules and storage space. When a module is hardware occupied, the user will fail to:

- read or write data to the module's registers or memories.
- disable the module clock.
- reset the module.

After hardware occupation is finished, the occupied module will be automatically reset. In addition, when the user performs a software reset to the master module, all the occupied modules will be reset at the same time.


31.5 Programming Procedures

31.5.1 ECDSA_DS Process

The overall ECDSA_DS process consists of the following five stages.

Figure 31.5-1. ECDSA_DS Process

The detailed programming procedures of each stage are described in the following sections.
```