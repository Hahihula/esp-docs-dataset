

# Chapter 10 Event Task Matrix (ETM)

## 10.1 Overview

The Event Task Matrix (ETM) peripheral contains 50 configurable channels. Each channel can map an event of any specified peripheral to a task of any specified peripheral. In this way, peripherals can be triggered to execute specified tasks without CPU intervention.

## 10.2 Features

The Event Task Matrix has the following features:

- Receive various events from multiple peripherals
- Generate various tasks for multiple peripherals
- 50 independently configurable ETM channels
- An ETM channel can be set up to receive any event, and map it to any task
- Each ETM channel can be enabled or disabled independently. If disabled, the channel will not respond to the configured event and generate the task mapped to that event
- Support for checking event and task status
- Peripherals supporting ETM include GPIO, LED PWM, general-purpose timers, RTC Timer, system timer, temperature sensor, ADC, I2S, GDMA, and PMU

Note that the 50 ETM channels are identical regarding their features and operations. Thus, in the following sections, ETM channels are collectively referred to as channeln (where n ranges from 0 to 49).

## 10.3 Functional Description

### 10.3.1 Architecture

The Event Task Matrix has 50 independent channels. Each channel can select any event as input, and map the event to any task as output (see Section 10.3.2 and Section 10.3.3 respectively). Each channel has an individual enable bit (see Section 10.3.6).