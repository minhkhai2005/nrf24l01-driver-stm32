# NRF24L01 Driver for STM32

This repository provides a lightweight and efficient C driver for interfacing STM32 microcontrollers with NRF24L01(+) 2.4GHz wireless transceivers. The implementation is designed for easy integration into embedded projects using STM32 MCUs.

## Features

- SPI-based communication with NRF24L01 modules
- Support for basic configuration (frequency, data rate, power, etc.)
- Simple transmit and receive API
- IRQ handling (if supported)
- Example code for initialization and data transfer

## Getting Started

### Prerequisites

- STM32 microcontroller (any series with SPI support)
- NRF24L01(+) module
- STM32 development environment (STM32CubeIDE, Keil, etc.)
- C compiler and toolchain

### Hardware Connections

| NRF24L01 Pin | STM32 Pin (example) |
|--------------|---------------------|
| VCC          | 3.3V                |
| GND          | GND                 |
| CE           | GPIO Output         |
| CSN/CS       | GPIO Output         |
| SCK          | SPI SCK             |
| MOSI         | SPI MOSI            |
| MISO         | SPI MISO            |
| IRQ          | GPIO Input (optional)|

### Installation

1. Clone this repository into your STM32 project:
    ```bash
    git clone https://github.com/minhkhai2005/nrf24l01-driver-stm32.git
    ```
2. Add the driver source files to your project.
3. Configure SPI and GPIO pins as required in your project settings.

### Usage Example

Visit https://minhkhai2005.github.io/nrf24l01-driver-stm32/index.html for more information

## License

This project is licensed under the MIT License.

## Acknowledgements

- Inspired by open-source STM32 and NRF24L01 projects

---

For any issues or contributions, please open an issue or submit a pull request.
