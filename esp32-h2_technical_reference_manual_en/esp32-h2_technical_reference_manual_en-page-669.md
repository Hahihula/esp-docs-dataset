

```markdown
occupied, the user will fail to:

* read or write data to the module's registers or memories.
* disable the module clock.
* reset the module.

At the end of the hardware occupation, the occupied module will be automatically reset. In addition, when user performs a software reset to the master module, all the occupied modules will be reset at the same time.
```

## 25.5 Programming Procedures

### 25.5.1 ECDSA Process

The overall ECDSA process consists of the following six stages.

![Figure 25.5-1. ECDSA Process](#)

Figure 25.5-1. ECDSA Process

The detailed programming procedures of each stage are described in the following sections.

#### 25.5.1.1 IDLE Stage

In the IDLE stage:

1. Configure the static parameters including eFuse bits:
   (a) **ECDSA_KEY**: The value of private key *d* in ECDSA. To correctly configure the key value in eFuse,
```