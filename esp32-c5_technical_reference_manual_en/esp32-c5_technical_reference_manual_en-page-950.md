

```markdown
## 28.4.3.3 Hardware Occupation

During the ECDSA operation, the following hardware modules will be occupied by ESP32-C5’s ECDSA accelerator:

* SHA Accelerator
* ECC Accelerator

Among them, the SHA accelerator will be released when `ECDSA_SHA_RELEASE_INT` is triggered, while the ECC accelerator will be occupied during the whole ECDSA operation.

**Note:**

Hardware occupation is a mechanism to protect multiplexed modules and storage space. When a module is hardware occupied, the user will fail to:

* read or write data to the module’s registers or memories.
* disable the module clock.
* reset the module.

After hardware occupation is finished, the occupied module will be automatically reset. In addition, when the user performs a software reset to the master module, all the occupied modules will be reset at the same time.
```

```markdown
## 28.5 Programming Procedures

### 28.5.1 ECDSA Process

The overall ECDSA process consists of the following six stages.
```