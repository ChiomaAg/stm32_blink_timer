# stm32_blink_timer
# STM32L432KC Blink LED with Timer Interrupts

This is a simple embedded project to toggle an LED on the STM32L432KC using timer interrupts.

## Features
- Uses TIM2 with MSI clock (32 kHz)
- Timer interrupt triggers every 1 second
- Toggles onboard LED on GPIOB Pin 3

## Build & Flash
- Developed with STM32CubeIDE
- Build using IDE or arm-none-eabi-gcc toolchain
- Flash with ST-Link or STM32CubeProgrammer

## Notes
- Timer configured with prescaler and period to achieve 1-second interrupts
- Interrupt handler toggles LED state in `HAL_TIM_PeriodElapsedCallback()`
