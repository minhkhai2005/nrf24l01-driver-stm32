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

```c
#include "nrf24l01.h"

// Initialize SPI and GPIO peripherals first

nrf24_init(&hspi1, CE_GPIO_Port, CE_Pin, CSN_GPIO_Port, CSN_Pin);

nrf24_config(2, 32); // Set channel and payload

nrf24_tx_mode(my_address, 32);
nrf24_send(data_buffer);
```

## API Reference

- `nrf24_init()`: Initialize the driver with SPI and GPIO handles
- `nrf24_config(channel, payload_len)`: Configure radio parameters
- `nrf24_tx_mode(address, length)`: Set TX mode
- `nrf24_rx_mode(address, length)`: Set RX mode
- `nrf24_send(buffer)`: Transmit data
- `nrf24_receive(buffer)`: Receive data

## License

This project is licensed under the MIT License.

## Acknowledgements

- Inspired by open-source STM32 and NRF24L01 projects

---

For any issues or contributions, please open an issue or submit a pull request.
