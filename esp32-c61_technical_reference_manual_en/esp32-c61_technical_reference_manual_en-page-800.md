

```markdown
Note:

Hardware occupation is a mechanism to protect multiplexed modules and storage space. When a module is hardware occupied, the user will fail to:
* read or write data to the module's registers or memories.
* disable the module clock.
* reset the module.

After hardware occupation is finished, the occupied module will be automatically reset. In addition, when the user performs a software reset to the master module, all the occupied modules will be reset at the same time.
```

## 22.5 Programming Procedures

### 22.5.1 ECDSA Process

The overall ECDSA process consists of the following six stages.

![Figure 22.5-1. ECDSA Process](#)

---

#### 22.5.1.1 IDLE Stage

In the IDLE stage:
```markdown
Espressif Systems    800        ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback   PRELIMINARY
```
```