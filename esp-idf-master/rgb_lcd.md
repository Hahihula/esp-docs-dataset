---
original_file_path: api-reference/peripherals/lcd/rgb_lcd.rst
---

# RGB Interfaced LCD

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

RGB LCD panel is created by `esp_lcd_new_rgb_panel`{.interpreted-text role="cpp:func"}, with various configurations specified in `esp_lcd_rgb_panel_config_t`{.interpreted-text role="cpp:type"}.

> - `esp_lcd_rgb_panel_config_t::clk_src`{.interpreted-text role="cpp:member"} selects the clock source of the RGB LCD controller. The available clock sources are listed in `lcd_clock_source_t`{.interpreted-text role="cpp:type"}.
> - `esp_lcd_rgb_panel_config_t::data_width`{.interpreted-text role="cpp:member"} sets number of data lines consumed by the RGB interface. It can be 8/16/24.
> - `esp_lcd_rgb_panel_config_t::bits_per_pixel`{.interpreted-text role="cpp:member"} specifies the number of bits per pixel. This differs from `esp_lcd_rgb_panel_config_t::data_width`{.interpreted-text role="cpp:member"}. By default, if this field is set to 0, the driver will automatically match the bpp to the value set in `esp_lcd_rgb_panel_config_t::data_width`{.interpreted-text role="cpp:member"}. However, in some scenarios, these values need to be different. For instance, a serial RGB interfaced LCD might only require `8` data lines, but the color depth could be `RGB888`, meaning `esp_lcd_rgb_panel_config_t::bits_per_pixel`{.interpreted-text role="cpp:member"} should be set to `24`.
> - `esp_lcd_rgb_panel_config_t::hsync_gpio_num`{.interpreted-text role="cpp:member"}, `esp_lcd_rgb_panel_config_t::vsync_gpio_num`{.interpreted-text role="cpp:member"}, `esp_lcd_rgb_panel_config_t::de_gpio_num`{.interpreted-text role="cpp:member"}, `esp_lcd_rgb_panel_config_t::pclk_gpio_num`{.interpreted-text role="cpp:member"}, `esp_lcd_rgb_panel_config_t::disp_gpio_num`{.interpreted-text role="cpp:member"} and `esp_lcd_rgb_panel_config_t::data_gpio_nums`{.interpreted-text role="cpp:member"} are GPIO pins consumed by the RGB LCD controller. If any of them are not used, please set them to `-1`.
> - `esp_lcd_rgb_panel_config_t::dma_burst_size`{.interpreted-text role="cpp:member"} specifies the size of the DMA transfer burst. Ensure this value is a power of 2.
> - `esp_lcd_rgb_panel_config_t::bounce_buffer_size_px`{.interpreted-text role="cpp:member"} specifies the size of the bounce buffer. This is required only for the \"bounce buffer\" mode. For more details, see `bounce_buffer_with_single_psram_frame_buffer`{.interpreted-text role="ref"}.
> - `esp_lcd_rgb_panel_config_t::timings`{.interpreted-text role="cpp:member"} specifies the timing parameters unique to the LCD panel. These parameters, detailed in `esp_lcd_rgb_timing_t`{.interpreted-text role="cpp:type"}, include the LCD resolution and blanking porches. Ensure they are set according to your LCD\'s datasheet.
> - `esp_lcd_rgb_panel_config_t::fb_in_psram`{.interpreted-text role="cpp:member"} determines if the frame buffer should be allocated from PSRAM. For further details, see `single_frame_buffer_in_psram`{.interpreted-text role="ref"}.
> - `esp_lcd_rgb_panel_config_t::num_fbs`{.interpreted-text role="cpp:member"} specifies how many frame buffers the driver should allocate. For backward compatibility, setting this to `0` will allocate a single frame buffer. If you don\'t want to allocate any frame buffer, use `esp_lcd_rgb_panel_config_t::no_fb`{.interpreted-text role="cpp:member"} instead.
> - `esp_lcd_rgb_panel_config_t::no_fb`{.interpreted-text role="cpp:member"} determines whether frame buffer will be allocated. When it is set, no frame buffer will be allocated. This is also called the `bounce_buffer_only`{.interpreted-text role="ref"} mode.

## RGB LCD Frame Buffer Operation Modes

Most of the time, the RGB LCD driver should maintain at least one screen sized frame buffer. According to the number and location of the frame buffer, the driver provides several different buffer modes.

### Single Frame Buffer in Internal Memory

This is the default and simplest and you do not have to specify flags or bounce buffer options. A frame buffer is allocated from the internal memory. The frame data is read out by DMA to the LCD verbatim. It needs no CPU intervention to function, but it has the downside that it uses up a fair bit of the limited amount of internal memory.

``` c
esp_lcd_panel_handle_t panel_handle = NULL;
esp_lcd_rgb_panel_config_t panel_config = {
    .data_width = 16, // RGB565 in parallel mode, thus 16 bits in width
    .clk_src = LCD_CLK_SRC_DEFAULT,
    .disp_gpio_num = EXAMPLE_PIN_NUM_DISP_EN,
    .pclk_gpio_num = EXAMPLE_PIN_NUM_PCLK,
    .vsync_gpio_num = EXAMPLE_PIN_NUM_VSYNC,
    .hsync_gpio_num = EXAMPLE_PIN_NUM_HSYNC,
    .de_gpio_num = EXAMPLE_PIN_NUM_DE,
    .data_gpio_nums = {
        EXAMPLE_PIN_NUM_DATA0,
        EXAMPLE_PIN_NUM_DATA1,
        EXAMPLE_PIN_NUM_DATA2,
        // other GPIOs
        // The number of GPIOs here should be the same to the value of "data_width" above
        ...
    },
    // The timing parameters should refer to your LCD spec
    .timings = {
        .pclk_hz = EXAMPLE_LCD_PIXEL_CLOCK_HZ,
        .h_res = EXAMPLE_LCD_H_RES,
        .v_res = EXAMPLE_LCD_V_RES,
        .hsync_back_porch = 40,
        .hsync_front_porch = 20,
        .hsync_pulse_width = 1,
        .vsync_back_porch = 8,
        .vsync_front_porch = 4,
        .vsync_pulse_width = 1,
    },
};
ESP_ERROR_CHECK(esp_lcd_new_rgb_panel(&panel_config, &panel_handle));
```

### Single Frame Buffer in PSRAM {#single_frame_buffer_in_psram}

If you have PSRAM and prefer to store the frame buffer there instead of using the limited internal memory, the LCD peripheral can utilize EDMA to fetch frame data directly from PSRAM, bypassing the internal cache. This can be enabled by setting `esp_lcd_rgb_panel_config_t::fb_in_psram`{.interpreted-text role="cpp:member"} to `true`. The trade-off is that when both the CPU and EDMA need access to PSRAM, the bandwidth is **shared** between them, meaning EDMA and the CPU each get half. If other peripherals are also using EDMA, a high pixel clock might cause LCD peripheral starvation, leading to display corruption. However, with a sufficiently low pixel clock, this approach minimizes CPU intervention.

::: only
esp32s3

The PSRAM shares the same SPI bus with the main flash (the one stores your firmware binary). At any given time, there can only be one consumer of the SPI bus. When you also use the main flash to serve your file system (e.g., `SPIFFS </api-reference/storage/spiffs>`{.interpreted-text role="doc"}), the bandwidth of the underlying SPI bus will also be shared, leading to display corruption. You can use `esp_lcd_rgb_panel_set_pclk`{.interpreted-text role="cpp:func"} to update the pixel clock frequency to a lower value.
:::

``` c
esp_lcd_panel_handle_t panel_handle = NULL;
esp_lcd_rgb_panel_config_t panel_config = {
    .data_width = 16, // RGB565 in parallel mode, thus 16 bits in width
    .clk_src = LCD_CLK_SRC_DEFAULT,
    .disp_gpio_num = EXAMPLE_PIN_NUM_DISP_EN,
    .pclk_gpio_num = EXAMPLE_PIN_NUM_PCLK,
    .vsync_gpio_num = EXAMPLE_PIN_NUM_VSYNC,
    .hsync_gpio_num = EXAMPLE_PIN_NUM_HSYNC,
    .de_gpio_num = EXAMPLE_PIN_NUM_DE,
    .data_gpio_nums = {
        EXAMPLE_PIN_NUM_DATA0,
        EXAMPLE_PIN_NUM_DATA1,
        EXAMPLE_PIN_NUM_DATA2,
        // other GPIOs
        // The number of GPIOs here should be the same to the value of "data_width" above
        ...
    },
    // The timing parameters should refer to your LCD spec
    .timings = {
        .pclk_hz = EXAMPLE_LCD_PIXEL_CLOCK_HZ,
        .h_res = EXAMPLE_LCD_H_RES,
        .v_res = EXAMPLE_LCD_V_RES,
        .hsync_back_porch = 40,
        .hsync_front_porch = 20,
        .hsync_pulse_width = 1,
        .vsync_back_porch = 8,
        .vsync_front_porch = 4,
        .vsync_pulse_width = 1,
    },
    .flags.fb_in_psram = true, // allocate frame buffer from PSRAM
};
ESP_ERROR_CHECK(esp_lcd_new_rgb_panel(&panel_config, &panel_handle));
```

### Double Frame Buffer in PSRAM {#double_frame_buffer_in_psram}

To prevent tearing effects, the simplest method is to use two screen-sized frame buffers. Given the limited internal memory, these buffers must be allocated from PSRAM. This ensures that the frame buffer being written to by the CPU and the one being read by the EDMA are always distinct and independent. The EDMA will only switch between the two buffers once the current write operation is complete and the frame has been fully transmitted to the LCD. The main drawback of this approach is the need to maintain synchronization between the two frame buffers.

``` c
esp_lcd_panel_handle_t panel_handle = NULL;
esp_lcd_rgb_panel_config_t panel_config = {
    .data_width = 16, // RGB565 in parallel mode, thus 16 bits in width
    .num_fbs = 2,     // allocate double frame buffer
    .clk_src = LCD_CLK_SRC_DEFAULT,
    .disp_gpio_num = EXAMPLE_PIN_NUM_DISP_EN,
    .pclk_gpio_num = EXAMPLE_PIN_NUM_PCLK,
    .vsync_gpio_num = EXAMPLE_PIN_NUM_VSYNC,
    .hsync_gpio_num = EXAMPLE_PIN_NUM_HSYNC,
    .de_gpio_num = EXAMPLE_PIN_NUM_DE,
    .data_gpio_nums = {
        EXAMPLE_PIN_NUM_DATA0,
        EXAMPLE_PIN_NUM_DATA1,
        EXAMPLE_PIN_NUM_DATA2,
        // other GPIOs
        // The number of GPIOs here should be the same to the value of "data_width" above
        ...
    },
    // The timing parameters should refer to your LCD spec
    .timings = {
        .pclk_hz = EXAMPLE_LCD_PIXEL_CLOCK_HZ,
        .h_res = EXAMPLE_LCD_H_RES,
        .v_res = EXAMPLE_LCD_V_RES,
        .hsync_back_porch = 40,
        .hsync_front_porch = 20,
        .hsync_pulse_width = 1,
        .vsync_back_porch = 8,
        .vsync_front_porch = 4,
        .vsync_pulse_width = 1,
    },
    .flags.fb_in_psram = true, // allocate frame buffer from PSRAM
};
ESP_ERROR_CHECK(esp_lcd_new_rgb_panel(&panel_config, &panel_handle));
```

### User Custom Frame Buffer {#user_custom_frame_buffer}

User can provide their own frame buffer instead of letting the driver allocate it. In this mode, user needs to manage the lifecycle of the frame buffer by themselves.

``` c
esp_lcd_panel_handle_t panel_handle = NULL;
esp_lcd_rgb_panel_config_t panel_config = {
    .data_width = 16, // RGB565 in parallel mode, thus 16 bits in width
    .clk_src = LCD_CLK_SRC_DEFAULT,
    .disp_gpio_num = EXAMPLE_PIN_NUM_DISP_EN,
    .pclk_gpio_num = EXAMPLE_PIN_NUM_PCLK,
    .vsync_gpio_num = EXAMPLE_PIN_NUM_VSYNC,
    .hsync_gpio_num = EXAMPLE_PIN_NUM_HSYNC,
    .de_gpio_num = EXAMPLE_PIN_NUM_DE,
    .data_gpio_nums = {
        EXAMPLE_PIN_NUM_DATA0,
        EXAMPLE_PIN_NUM_DATA1,
        EXAMPLE_PIN_NUM_DATA2,
        // other GPIOs
        // The number of GPIOs here should be the same to the value of "data_width" above
        ...
    },
    // The timing parameters should refer to your LCD spec
    .timings = {
        .pclk_hz = EXAMPLE_LCD_PIXEL_CLOCK_HZ,
        .h_res = EXAMPLE_LCD_H_RES,
        .v_res = EXAMPLE_LCD_V_RES,
        .hsync_back_porch = 40,
        .hsync_front_porch = 20,
        .hsync_pulse_width = 1,
        .vsync_back_porch = 8,
        .vsync_front_porch = 4,
        .vsync_pulse_width = 1,
    },
    .user_fbs[0] = user_frame_buffer, // use user custom frame buffer
};
ESP_ERROR_CHECK(esp_lcd_new_rgb_panel(&panel_config, &panel_handle));
```

### Bounce Buffer with Single PSRAM Frame Buffer {#bounce_buffer_with_single_psram_frame_buffer}

This mode allocates two \"bounce buffers\" from internal memory and a main frame buffer in PSRAM. To enable this mode, set the `esp_lcd_rgb_panel_config_t::fb_in_psram`{.interpreted-text role="cpp:member"} flag and specify a non-zero value for `esp_lcd_rgb_panel_config_t::bounce_buffer_size_px`{.interpreted-text role="cpp:member"}. The bounce buffers only need to hold a few lines of display data, which is much smaller than the main frame buffer. The LCD peripheral uses DMA to read data from one bounce buffer while an interrupt routine uses the CPU DCache to copy data from the main PSRAM frame buffer into the other bounce buffer. Once the LCD peripheral finishes reading from the bounce buffer, the buffers swap roles, allowing the CPU to fill the other one. The advantage of this mode is achieving a higher pixel clock frequency. Since the bounce buffers are larger than the FIFOs in the EDMA path, this method is also more robust against short bandwidth spikes. The downside is a significant increase in CPU usage, and the LCD **CANNOT** function if the external memory cache is disabled, such as during OTA or NVS writes to the main flash.

:::: note
::: title
Note
:::

For optimal performance in this mode, it is highly recommended to enable the \"PSRAM XIP (Execute In Place)\" feature by turning on the Kconfig option: `CONFIG_SPIRAM_XIP_FROM_PSRAM`{.interpreted-text role="ref"}. This allows the CPU to fetch instructions and read-only data directly from PSRAM instead of the main flash. Additionally, the external memory cache remains active even when writing to the main flash via SPI 1, making it feasible to display an OTA progress bar during your application updates.
::::

:::: note
::: title
Note
:::

This mode also faces issues due to limited PSRAM bandwidth. For instance, if your draw buffers are in PSRAM and their contents are copied to the internal frame buffer by CPU Core 1, while CPU Core 0 is performing another memory copy in the DMA EOF ISR, both CPUs will be accessing PSRAM via cache, sharing its bandwidth. This significantly increases the memory copy time in the DMA EOF ISR, causing the driver to fail in switching the bounce buffer promptly, resulting in a screen shift. Although the driver can detect this condition and restart in the LCD\'s VSYNC interrupt handler, you may still notice flickering on the screen.
::::

``` c
esp_lcd_panel_handle_t panel_handle = NULL;
esp_lcd_rgb_panel_config_t panel_config = {
    .data_width = 16, // RGB565 in parallel mode, thus 16 bits in width
    .clk_src = LCD_CLK_SRC_DEFAULT,
    .bounce_buffer_size_px = 10 * EXAMPLE_LCD_H_RES, // allocate 10 lines data as bounce buffer from internal memory
    .disp_gpio_num = EXAMPLE_PIN_NUM_DISP_EN,
    .pclk_gpio_num = EXAMPLE_PIN_NUM_PCLK,
    .vsync_gpio_num = EXAMPLE_PIN_NUM_VSYNC,
    .hsync_gpio_num = EXAMPLE_PIN_NUM_HSYNC,
    .de_gpio_num = EXAMPLE_PIN_NUM_DE,
    .data_gpio_nums = {
        EXAMPLE_PIN_NUM_DATA0,
        EXAMPLE_PIN_NUM_DATA1,
        EXAMPLE_PIN_NUM_DATA2,
        // other GPIOs
        // The number of GPIOs here should be the same to the value of "data_width" above
        ...
    },
    // The timing parameters should refer to your LCD spec
    .timings = {
        .pclk_hz = EXAMPLE_LCD_PIXEL_CLOCK_HZ,
        .h_res = EXAMPLE_LCD_H_RES,
        .v_res = EXAMPLE_LCD_V_RES,
        .hsync_back_porch = 40,
        .hsync_front_porch = 20,
        .hsync_pulse_width = 1,
        .vsync_back_porch = 8,
        .vsync_front_porch = 4,
        .vsync_pulse_width = 1,
    },
    .flags.fb_in_psram = true, // allocate frame buffer from PSRAM
};
ESP_ERROR_CHECK(esp_lcd_new_rgb_panel(&panel_config, &panel_handle));
```

### Bounce Buffer Only {#bounce_buffer_only}

This mode is similar to `bounce_buffer_with_single_psram_frame_buffer`{.interpreted-text role="ref"}, but there is no PSRAM frame buffer initialized by the LCD driver. Instead, the user supplies a callback function that is responsible for filling the bounce buffers. As this driver does not care where the written pixels come from, this allows for the callback doing e.g., on-the-fly conversion from a smaller, 8-bit-per-pixel PSRAM frame buffer to a 16-bit LCD, or even procedurally generated frame-buffer-less graphics. This option is selected by setting the `esp_lcd_rgb_panel_config_t::no_fb`{.interpreted-text role="cpp:member"} flag and supplying a `esp_lcd_rgb_panel_config_t::bounce_buffer_size_px`{.interpreted-text role="cpp:member"} value. And then register the `esp_lcd_rgb_panel_event_callbacks_t::on_bounce_empty`{.interpreted-text role="cpp:member"} callback by calling `esp_lcd_rgb_panel_register_event_callbacks`{.interpreted-text role="cpp:func"}.

:::: note
::: title
Note
:::

In a well-designed embedded application, situations where the DMA cannot deliver data as fast as the LCD consumes it should be avoided. However, such scenarios can theoretically occur. In the {IDF_TARGET_NAME} hardware, this results in the LCD outputting dummy bytes while the DMA waits for data. If the DMA were to run in a continuous stream, it could cause a desynchronization between the LCD address from which the DMA reads data and the address from which the LCD peripheral outputs data, leading to a **permanently** shifted image. To prevent this, you can either enable the `CONFIG_LCD_RGB_RESTART_IN_VSYNC`{.interpreted-text role="ref"} option, allowing the driver to automatically restart the DMA during the VBlank interrupt, or call `esp_lcd_rgb_panel_restart`{.interpreted-text role="cpp:func"} to manually restart the DMA. Note that `esp_lcd_rgb_panel_restart`{.interpreted-text role="cpp:func"} does not restart the DMA immediately; instead, the DMA will be restarted at the next VSYNC event.
::::

## API Reference

::: include-build-file
inc/esp_lcd_panel_rgb.inc
:::
