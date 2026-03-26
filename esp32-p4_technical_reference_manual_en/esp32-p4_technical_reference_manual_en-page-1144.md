

```markdown
Chapter 19 Permission Control (PMS)

GoBack

Since LP CPU only supports machine mode, HP APM and LP APM grant access permissions for the machine mode of LP CPU.

DMA masters can access slaves regardless of the CPUs' work mode. DMA APM provides separate read and write permissions for each DMA master.

19.4.1 Configuring Access Permissions for HP CPU0/1

The configuration process for HP CPU0/1 accessing internal memory, external memory, or peripheral registers is as follows:

1. Configure user mode or machine mode for HP CPU0/1. For how to configure the work mode, please refer to RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10.

2. If accessing peripheral registers, eight additional address ranges can be configured, please refer to Section 19.3.2 for details.

3. Configure access permissions:

- Configure the access permissions to internal memory (HP L2MEM and HP ROM), external memory (External RAM and flash), and peripheral registers (HP PERI and HP CPU PERI) in the HP system through HP_PERI_PMS_REG:
  - Configure the permission of HP CPU accessing the MODULE_NAME module in MODE_NAME mode using PMS_COREn_MODE_NAME_MODULE_NAME_ALLOW, for example PMS_COREn_MM_PSram_ALLOW.

- Configure the access permissions to LP SRAM and LP PERI through HP2LP_PERI_PMS_REG:
  - Configure the permission of HP CPU accessing the MODULE_NAME module in MODE_NAME mode using PMS_HP_COREn_MODE_NAME_MODULE_NAME_ALLOW, for example PMS_HP_COREn_MM_LP_SYSREG_ALLOW.

19.4.2 Configuring Access Permissions for LP CPU

LP CPU only supports machine mode. The configuration process for LP CPU accessing internal memory, external memory, or peripheral registers is as follows:

1. If accessing peripheral registers, eight additional address ranges can be configured, please refer to Section 19.3.2 for details.

2. Configure access permissions:

- Configure the access permissions to internal memory (HP L2MEM and HP ROM), external memory (External RAM and flash), and peripheral registers (HP PERI and HP CPU PERI) in the HP system through LP2HP_PERI_PMS_REG:
  - Configure the permission of LP CPU accessing the MODULE_NAME module in machine mode using PMS_LP_MM_MODULE_NAME_ALLOW, for example PMS_LP_MM_PSram_ALLOW.

- Configure the access permissions to peripheral registers (LP PERI) in the LP system through LP_PERI_PMS_REG:
  - Configure the permission of LP CPU accessing the MODULE_NAME module in machine mode using PMS_LP_MM_MODULE_NAME_ALLOW, for example PMS_LP_MM_LP_SYSREG_ALLOW.
```