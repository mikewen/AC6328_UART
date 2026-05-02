# AC6328 UART to BLE Bridge

[![Platform](https://img.shields.io/badge/platform-AC6328-blue.svg)](https://github.com/mikewen/AC6328_UART)
[![Language](https://img.shields.io/badge/language-C-green.svg)](https://github.com/mikewen/AC6328_UART)

A firmware project for the **Jieli AC6328** Bluetooth chip that implements a **UART to BLE (Bluetooth Low Energy) Bridge**. It reads data from the hardware UART port and transmits it wirelessly via BLE notifications.

## 📖 Overview

This project implements a firmware solution for the Jieli AC6328 Bluetooth chip that reads data from its hardware UART port and transmits it wirelessly via BLE (Bluetooth Low Energy) notifications.

Unlike standard AT-command-based modules that require a host MCU, this project allows the AC6328 to operate as a standalone UART-to-BLE bridge. This makes it ideal for converting traditional serial data streams into modern wireless BLE communication.

## ✨ Features

- **Full-duplex UART communication** on dedicated hardware pins
- **BLE notification transmission** of received UART data
- **Configurable UART parameters**: Baud rate, data bits, stop bits, parity
- **Efficient data handling** using DMA or interrupt-driven modes
- **Low power consumption** suitable for battery-powered applications

## 🔧 Hardware Requirements

| Component | Description |
|-----------|-------------|
| **MCU** | Jieli AC6328 (Bluetooth 5.1 dual-mode SoC) |
| **UART Pins** | TX: IO_PORT_DP, RX: IO_PORT_DM |
| **Clock** | 24MHz external crystal oscillator |
| **Voltage** | 1.8V - 3.4V |

> **Note on UART Pins**: On the AC6328, the USB DP (D+) and DM (D-) pins can be configured for UART communication when USB functionality is not required.

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/mikewen/AC6328_UART.git
cd AC6328_UART