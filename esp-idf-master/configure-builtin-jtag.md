---
original_file_path: api-guides/jtag-debugging/configure-builtin-jtag.rst
---

# Configure {IDF_TARGET_NAME} Built-in JTAG Interface

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

{IDF_TARGET_JTAG_PIN_Dneg:default=\"Not Updated!\", esp32c3=\"GPIO18\", esp32c6=\"GPIO12\", esp32s3=\"GPIO19\", esp32h2=\"GPIO26\", esp32p4=\"GPIO24\"} {IDF_TARGET_JTAG_PIN_Dpos:default=\"Not Updated!\", esp32c3=\"GPIO19\", esp32c6=\"GPIO13\", esp32s3=\"GPIO20\", esp32h2=\"GPIO27\", esp32p4=\"GPIO25\"}

{IDF_TARGET_NAME} has built-in JTAG circuitry and can be debugged without any additional chip. Only a USB cable connected to the D+/D- pins is necessary. For dev kits without an exposed USB Serial Jtag connector, a USB breakout cable can be used. The necessary connections are shown in the following section.

## Configure Hardware

  ----------------------------------------------------------------------------------
  {IDF_TARGET_NAME} Pin        USB Signal
  ---------------------------- -----------------------------------------------------
  {IDF_TARGET_JTAG_PIN_Dneg}   D-

  {IDF_TARGET_JTAG_PIN_Dpos}   D+

  5V                           V_BUS

  GND                          Ground
  ----------------------------------------------------------------------------------

  : {IDF_TARGET_NAME} pins and USB signals

Please verify that the {IDF_TARGET_NAME} pins used for USB communication are not connected to some other HW that may disturb the JTAG operation.

## Configure USB Drivers

JTAG communication should work on all supported platforms. Windows and Linux require extra steps as described below.

### Windows

Windows users might get [LIBUSB_ERROR_NOT_FOUND]{.title-ref} errors. To resolve this, install drivers using one of the following methods:

- In `Espressif Installation Manager (EIM) <../../get-started/windows-setup>`{.interpreted-text role="doc"} graphical user interface (GUI), click `Open Dashboard` under `Manage Installations`, and then click `Install Drivers`:

  > <figure class="align-center">
  > <img src="../../../_static/jtag-debugging-install-usb-drivers-eim.png" alt="Install Drivers in EIM GUI" />
  > <figcaption aria-hidden="true">Install Drivers in EIM GUI</figcaption>
  > </figure>

- Run the following command from PowerShell to install drivers with EIM command line interface:

  > ``` bash
  > eim install-drivers
  > ```

- Run the following command from PowerShell to install drivers with [idf-env](https://github.com/espressif/idf-env):

  > ``` bash
  > Invoke-WebRequest 'https://dl.espressif.com/dl/idf-env/idf-env.exe' -OutFile .\idf-env.exe; .\idf-env.exe driver install --espressif
  > ```

### Linux

On Linux adding OpenOCD udev rules is required and is done by placing the following [udev rules file](https://github.com/espressif/openocd-esp32/blob/master/contrib/60-openocd.rules) in the `/etc/udev/rules.d` folder.
