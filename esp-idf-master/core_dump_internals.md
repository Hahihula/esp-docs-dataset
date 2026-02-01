---
original_file_path: api-guides/core_dump_internals.rst
---

# Anatomy of Core Dump Image

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

Core dump files are generated in ELF format, which provides comprehensive information regarding the software\'s state at the moment the crash occurs, including CPU registers and memory contents.

The memory state embeds a snapshot of all tasks mapped in the memory space of the program. The CPU state contains register values when the core dump has been generated. The core dump file uses a subset of the ELF structures to register this information.

Loadable ELF segments are used to store the process\' memory state, while ELF notes (`ELF.PT_NOTE`) are used to store the process\' metadata (e.g., PID, registers, signal etc). In particular, the CPU\'s status is stored in a note with a special name and type (`CORE`, `NT_PRSTATUS type`).

Here is an overview of the core dump layout:

<figure class="align-center">
<img src="../../_static/core_dump_format_elf.png" alt="Core Dump ELF Image Format" />
<figcaption aria-hidden="true">Core Dump ELF Image Format</figcaption>
</figure>

:::: note
::: title
Note
:::

The format of the image file shown in the above pictures represents the current version of the image and can be changed in future releases.
::::

# Overview of Implementation

The figure below describes some basic aspects related to the implementation of the core dump:

<figure class="align-center">
<img src="../../_static/core_dump_impl.png" alt="Core Dump Implementation Overview" />
<figcaption aria-hidden="true">Core Dump Implementation Overview</figcaption>
</figure>

:::: note
::: title
Note
:::

The diagram above hides some details and represents the current implementation of the core dump which can be changed later.
::::
