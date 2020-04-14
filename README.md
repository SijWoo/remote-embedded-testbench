# remote-embedded-testbench
Testbench to let debug embedded system projects remotely through ssh.

The plan is to create a board that can be controlled with a serial terminal to debug embedded system projects remotely. The testbench board will have configurable I/O, communication protocols (SPI, I2C, UART, etc.), ADC, DAC, logic anyalyzer ports, power management, and measurements. 

## Background
Most embedded system engineers need to have the hardware physically with them to get any work done. Some teams may only have a limited number of hardware components so each engineer may not have a personal copy. Due to the recent pandemic at the time of writing, engineers are in need of remotely accessible embedded hardware. This project will allow engineers to monitor and control pins, send data through any of the low-speed communication protocols, debug with gdb, and automate testing all through SSH.

## Functionality
The testbench will power and interface with all the I/O pins of the embedded system to be tested (subject). The testbench will be able to do the following:
1. Power the subject
2. Monitor the power draw of the subject
3. Control digital pins of the subject
4. Transmit and receive data packets through SPI, I2C, UART, CAN to the subject
5. Create analog voltage with DAC
6. Pinouts for logic analyzer and oscilloscope

## How it works
The testbench board will be connected through USB to a computer with SSH enabled. The testbench
