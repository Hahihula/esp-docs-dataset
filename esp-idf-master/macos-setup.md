---
original_file_path: get-started/macos-setup.rst
---

# Installation of ESP-IDF and Tools on macOS

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

This section describes how to install ESP-IDF and its required tools on macOS using the Espressif Installation Manager (EIM).

:::: note
::: title
Note
:::

This document describes the default and recommended way to install ESP-IDF v6.0 and newer versions. ESP-IDF also supports the `legacy installation method on macOS <linux-macos-setup-legacy>`{.interpreted-text role="doc"}, which was the default before ESP-IDF v6.0.
::::

## Step 1: Install the Prerequisites

Install the required prerequisites via [Homebrew](https://brew.sh/):

``` bash
brew install libgcrypt glib pixman sdl2 libslirp dfu-util cmake python
```

:::: note
::: title
Note
:::

Python 3.10 is the minimum supported version for ESP-IDF.

However, for [Offline Installation](#offline-installation), EIM requires **Python 3.11 or versions later**.
::::

## Step 2: Install the EIM

Add the EIM repository to the Homebrew to make it available for installation:

``` bash
brew tap espressif/eim
```

Then, install the EIM Graphical User Interface (GUI) or Command Line Interface (CLI) via Homebrew:

- 

  GUI:

  :   ``` bash
      brew install --cask eim-gui
      ```

- 

  CLI:

  :   ``` bash
      brew install eim
      ```

:::: note
::: title
Note
:::

Installing via Homebrew makes it easier to keep EIM up to date.

Alternatively, download the EIM installer for macOS from the [Espressif Download Page](https://dl.espressif.com/dl/eim/), which provides both online and offline installers available in both CLI and GUI versions.
::::

## Step 3: Install ESP-IDF Using EIM

You can install ESP-IDF and the required tools using one of the following methods, depending on your preference:

- [Online Installation Using EIM GUI](#online-installation-using-eim-gui)

  Recommended for most users. Installs ESP-IDF and tools via a graphical interface with internet access.

- [Online Installation Using EIM CLI](#online-installation-using-eim-cli)

  Installs ESP-IDF and tools from the command line with internet access.

- [Online Installation Using a Loaded Configuration](#online-installation-using-a-loaded-configuration)

  Installs ESP-IDF and tools using a pre-saved configuration file copied from another PC. This method works with both the GUI and CLI, but requires internet access.

- [Offline Installation](#offline-installation)

  Installs ESP-IDF and tools from a local package, without internet access.

### Online Installation Using EIM GUI

Open the ESP-IDF Installation Manager application [eim]{.title-ref}.

Under `New Installation` click `Start Installation`.

<figure class="align-center">
<img src="../../_static/get-started-eim-gui.png" alt="EIM Start Installation" />
<figcaption aria-hidden="true">EIM Start Installation</figcaption>
</figure>

:::: note
::: title
Note
:::

If you have never installed ESP-IDF before, you will not see `Manage Installations`. In this case, `New Installation` will be the only available option.
::::

Under `Easy Installation`, click `Start Easy Installation` to install the latest stable version of ESP-IDF with default settings.

<figure class="align-center">
<img src="../../_static/get-started-eim-gui-install.png" alt="EIM Easy Installation" />
<figcaption aria-hidden="true">EIM Easy Installation</figcaption>
</figure>

If all prerequisites and path checks pass, you will see the `Ready to Install` page. Click `Start Installation` to begin the installation.

<figure class="align-center">
<img src="../../_static/get-started-eim-gui-ready-install.png" alt="EIM Ready to Install" />
<figcaption aria-hidden="true">EIM Ready to Install</figcaption>
</figure>

During the installation, you can monitor the progress directly in the interface.

<figure class="align-center">
<img src="../../_static/get-started-eim-gui-installing.png" alt="EIM Installing" />
<figcaption aria-hidden="true">EIM Installing</figcaption>
</figure>

Once finished, the `Installation Complete` page will appear.

<figure class="align-center">
<img src="../../_static/get-started-eim-gui-install-complete.png" alt="EIM Installation Complete" />
<figcaption aria-hidden="true">EIM Installation Complete</figcaption>
</figure>

If the installation fails, you can:

- Click `Logs` at the bottom of the interface to view error details. Resolve the issues and click `Try Again` to restart the installation.
- Alternatively, use [Custom Installation](https://docs.espressif.com/projects/idf-im-ui/en/latest/expert_installation.html).

:::: note
::: title
Note
:::

- To select an ESP-IDF version or customize the installation path, use `Custom Installation` instead. See more instructions in [EIM documentation \> Expert Installations](https://docs.espressif.com/projects/idf-im-ui/en/latest/expert_installation.html).
- To manage existing installations, refer to [EIM documentation \> Version Management](https://docs.espressif.com/projects/idf-im-ui/en/latest/version_management.html).
::::

### Online Installation Using EIM CLI

Run the following command to install the latest stable version of ESP-IDF with default settings in non-interactive mode:

``` bash
eim install
```

If you encounter issues running the above command, or if you want to customize the installation path, select ESP-IDF versions, or modify other options, launch the interactive installation wizard and follow the on-screen prompts:

``` bash
eim wizard
```

If the ESP-IDF version you want to install is not available in the interactive wizard, run the following command to install any available [versions](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/versions.html#releases). For example, to install ESP-IDF v5.4.2, run:

``` bash
eim install -i v5.4.2
```

Once the installation is complete, you will see the following message in the terminal:

``` bash
2025-11-03T15:54:12.537993300+08:00 - INFO - Wizard result: %{r}
2025-11-03T15:54:12.544174+08:00 - INFO - Successfully installed IDF
2025-11-03T15:54:12.545913900+08:00 - INFO - Now you can start using IDF tools
```

:::: note
::: title
Note
:::

- 

  To see all available options, run:

  :   ``` bash
      eim --help
      ```

- For more information about CLI usage, refer to
  - [EIM documentation \> CLI Configuration](https://docs.espressif.com/projects/idf-im-ui/en/latest/cli_configuration.html)
  - [EIM documentation \> CLI Commands](https://docs.espressif.com/projects/idf-im-ui/en/latest/cli_commands.html)
::::

### Online Installation Using a Loaded Configuration

When you install ESP-IDF, the installer automatically saves your setup to a configuration file named `eim_config.toml` in the installation directory. This configuration file can be reused on other computers to reproduce the same installation setup.

To install ESP-IDF using an existing `eim_config.toml` file, refer to the [EIM documentation \> Configuration Files](https://docs.espressif.com/projects/idf-im-ui/en/latest/gui_configuration.html#configuration-files).

### Offline Installation

Both the GUI and CLI installers support offline installation. For instructions, refer to [EIM documentation \> Offline Installation](https://docs.espressif.com/projects/idf-im-ui/en/latest/offline_installation.html).

## Next Steps

You are now ready to start developing with ESP-IDF. To begin building and running your first application, continue with the `get-started-build`{.interpreted-text role="ref"} section.

::: {.toctree hidden="" maxdepth="1" caption="Legacy Installation"}
linux-macos-setup-legacy
:::
