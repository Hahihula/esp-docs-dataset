---
original_file_path: api-reference/peripherals/lcd/parl_lcd.rst
---

# Parallel IO simulation of SPI or I80 Interfaced LCD

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

Parallel IO is not a bus-type peripheral. The driver directly creates a Parallel IO device for the LCD. Currently the driver supports SPI (1 bit data width) and I80 (8 bit data width) modes.

1.  Create Parallel IO device by `esp_lcd_new_panel_io_parl`{.interpreted-text role="cpp:func"}. You need to set up the following parameters for a Parallel IO device:

    > - `esp_lcd_panel_io_parl_config_t::clk_src`{.interpreted-text role="cpp:member"} sets the clock source of the Parallel IO device. Note, the default clock source may be different between ESP targets.
    > - `esp_lcd_panel_io_parl_config_t::clk_gpio_num`{.interpreted-text role="cpp:member"} sets the GPIO number of the pixel clock (also referred as `WR` or `SCLK` in some LCD spec)
    > - `esp_lcd_panel_io_parl_config_t::dc_gpio_num`{.interpreted-text role="cpp:member"} sets the GPIO number of the data or command select pin (also referred as `RS` in some LCD spec)
    > - `esp_lcd_panel_io_parl_config_t::cs_gpio_num`{.interpreted-text role="cpp:member"} sets the GPIO number of the chip select pin. (Note that the Parallel IO LCD driver only supports a single LCD device).
    > - `esp_lcd_panel_io_parl_config_t::data_width`{.interpreted-text role="cpp:member"} sets the bit width of the data bus (only support `1` or `8`)
    > - `esp_lcd_panel_io_parl_config_t::data_gpio_nums`{.interpreted-text role="cpp:member"} is the array of the GPIO number of the data bus. The number of GPIOs should be equal to the `esp_lcd_panel_io_parl_config_t::data_width`{.interpreted-text role="cpp:member"} value.
    > - `esp_lcd_panel_io_parl_config_t::max_transfer_bytes`{.interpreted-text role="cpp:member"} sets the maximum number of bytes that can be transferred in one transaction.
    > - `esp_lcd_panel_io_parl_config_t::dma_burst_size`{.interpreted-text role="cpp:member"} sets the number of bytes transferred by dma burst.
    > - `esp_lcd_panel_io_parl_config_t::pclk_hz`{.interpreted-text role="cpp:member"} sets the pixel clock frequency in Hz. Higher pixel clock frequency results in higher refresh rate, but may cause display abnormalities if the DMA bandwidth is not sufficient or the LCD controller chip does not support high pixel clock frequency.
    > - `esp_lcd_panel_io_parl_config_t::dc_levels`{.interpreted-text role="cpp:member"} sets the effective level for DC data selection and command selection.
    > - `esp_lcd_panel_io_parl_config_t::lcd_cmd_bits`{.interpreted-text role="cpp:member"} and `esp_lcd_panel_io_parl_config_t::lcd_param_bits`{.interpreted-text role="cpp:member"} set the bit width of the command and parameter that recognized by the LCD controller chip. This is chip specific, you should refer to your LCD spec in advance.
    > - `esp_lcd_panel_io_parl_config_t::trans_queue_depth`{.interpreted-text role="cpp:member"} sets the maximum number of transactions that can be queued in the Parallel IO device. A bigger value means more transactions can be queued up, but it also consumes more memory.
    >
    > ``` c
    > esp_lcd_panel_io_handle_t io_handle = NULL;
    > esp_lcd_panel_io_parl_config_t io_config = {
    >     .clk_src = PARLIO_CLK_SRC_DEFAULT,
    >     .dc_gpio_num = EXAMPLE_PIN_NUM_DC,
    >     .clk_gpio_num = EXAMPLE_PIN_NUM_PCLK,
    >     .data_gpio_nums = {
    >         EXAMPLE_PIN_NUM_DATA0, // set DATA0 to drive SPI interfaced LCD or set DATA0~7 to drive I80 interfaced LCD
    >     },
    >     .data_width = 1, // set 1 to drive SPI interfaced LCD or set 8 to drive I80 interfaced LCD
    >     .max_transfer_bytes = EXAMPLE_LCD_H_RES * 100 * sizeof(uint16_t), // transfer 100 lines of pixels (assume pixel is RGB565) at most in one transaction
    >     .dma_burst_size = EXAMPLE_DMA_BURST_SIZE,
    >     .cs_gpio_num = EXAMPLE_PIN_NUM_CS,
    >     .pclk_hz = EXAMPLE_LCD_PIXEL_CLOCK_HZ,
    >     .trans_queue_depth = 10,
    >     .dc_levels = {
    >         .dc_cmd_level = 0,
    >         .dc_data_level = 1,
    >     },
    >     .lcd_cmd_bits = EXAMPLE_LCD_CMD_BITS,
    >     .lcd_param_bits = EXAMPLE_LCD_PARAM_BITS,
    > };
    >
    > ESP_ERROR_CHECK(esp_lcd_new_panel_io_parl(&io_config, io_handle));
    > ```
    >
    > ::::: only
    > not SOC_PARLIO_SUPPORT_I80_LCD
    >
    > :::: note
    > ::: title
    > Note
    > :::
    >
    > Due to hardware limitations, {IDF_TARGET_NAME} can not drive I80 interfaced LCD by Parallel IO.
    > ::::
    > :::::

2.  Install the LCD controller driver. The LCD controller driver is responsible for sending the commands and parameters to the LCD controller chip. In this step, you need to specify the Parallel IO device handle that allocated in the last step, and some panel specific configurations:

    > - `esp_lcd_panel_dev_config_t::reset_gpio_num`{.interpreted-text role="cpp:member"} sets the LCD\'s hardware reset GPIO number. If the LCD does not have a hardware reset pin, set this to `-1`.
    > - `esp_lcd_panel_dev_config_t::rgb_ele_order`{.interpreted-text role="cpp:member"} sets the RGB element order of each color data.
    > - `esp_lcd_panel_dev_config_t::bits_per_pixel`{.interpreted-text role="cpp:member"} sets the bit width of the pixel color data. The LCD driver uses this value to calculate the number of bytes to send to the LCD controller chip.
    > - `esp_lcd_panel_dev_config_t::data_endian`{.interpreted-text role="cpp:member"} specifies the data endian to be transmitted to the screen. No need to specify for color data within one byte, like RGB232. For drivers that do not support specifying data endian, this field would be ignored.
    >
    > ``` c
    > esp_lcd_panel_handle_t panel_handle = NULL;
    > esp_lcd_panel_dev_config_t panel_config = {
    >     .reset_gpio_num = EXAMPLE_PIN_NUM_RST,
    >     .rgb_ele_order = LCD_RGB_ELEMENT_ORDER_BGR,
    >     .bits_per_pixel = 16,
    > };
    > // Create LCD panel handle for ST7789, with the Parallel IO device handle
    > ESP_ERROR_CHECK(esp_lcd_new_panel_st7789(io_handle, &panel_config, &panel_handle));
    > ```

## API Reference

::: include-build-file
inc/esp_lcd_io_parl.inc
:::
