Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

Subtitle: GPIO input sync

Figure Caption:
- Figure 6.4-1. GPIO Input Synchronized on APB Clock Rising Edge or on Falling Edge.

Body Text:

Figure Description with Diagrams:
- The diagram shows a block labeled "First-stage synchronizer" and another labelled "Second-stage synchronizer". There are inputs to these blocks, including "gpio_pinX_sync1_bypass[0]", "gpio_pinX_sync1_bypass[1]", "gpio_pinX_sync2_bypass[0]", "gpio_pinX_sync2_bypass[1]", with arrows pointing towards them. The outputs from the first-stage synchronizer are labeled as "negtive sync" and "positive sync", which feed into a block that is not fully visible in this image.

Section Title: 6.4.3 Functional Description

Body Text:
To read GPIO pin \(X\^1\) into peripheral signal \(Y\), follow the steps below:

1. Configure register `GPIO FUNCy_IN SEL CFG REG` corresponding to peripheral signal \(Y\) in GPIO matrix:
   - Set `GPIO SIGy_IN SEL` to enable peripheral signal input via GPIO matrix.
   - Set `GPIO FUNCy_IN SEL` to the desired GPIO pin, i.e., \(X\^1\) here.

Note that some peripheral signals have no valid `GPIO SIGy_IN SEL` bit, namely these peripherals can only receive input signals via GPIO matrix.

2. Optionally enable the filter for pin input signals by setting the register `IO MUX FILTER EN`. Only the signals with a valid width of more than two APB clock cycles can be sampled, see Figure 6.4-2.

Figure Caption:
- Figure 6.4-2. Filter Timing of GPIO Input Signals

Body Text:

3. Synchronize GPIO input. To do so, please set `GPIO PINx REG` corresponding to GPIO pin \(X\) as follows:
   - Set `GPIO PINx SYNC1 BYPASS` to enable input signal synchronized on rising edge or on falling edge in the first clock, see Figure 6.4-1.

Footer Information:

- Page number: "475"
- Document title and version information at bottom right corner.
- Company name: Espressif Systems
- Link text for feedback submission is present but not described as it's a hyperlink element which I cannot extract the URL from in this format, so only its presence can be noted.