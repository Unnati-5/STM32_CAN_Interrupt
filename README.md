\# STM32 CAN Communication Using Interrupts



\## Overview



This project implements an \*\*interrupt-driven Controller Area Network (CAN)

communication system using the STM32F405 microcontroller\*\*.



The project demonstrates practical implementation of CAN communication at the

microcontroller level, including CAN peripheral configuration, CAN message

transmission and reception, interrupt-based message handling, CAN transceiver

interfacing, and UART-based monitoring.



The implementation is developed using \*\*STM32CubeIDE and STM32 HAL\*\*, with

the CAN communication handled using interrupts rather than continuous

polling.



\---



\## Key Features



\- STM32F405 microcontroller

\- CAN communication

\- CAN1 / CAN2 peripheral configuration

\- Interrupt-driven CAN message handling

\- CAN transmit and receive functionality

\- MCP2551 CAN transceiver interface

\- UART-based monitoring and debugging

\- Embedded C implementation

\- STM32 HAL drivers

\- STM32CubeIDE development environment



\---



\## Project Objective



The objective of this project is to develop and understand a practical

embedded CAN communication system using the STM32 microcontroller.



The project focuses on:



1\. Configuring the STM32 CAN peripheral.

2\. Establishing communication through a CAN transceiver.

3\. Transmitting CAN frames.

4\. Receiving CAN frames using interrupts.

5\. Processing received messages inside the interrupt/callback mechanism.

6\. Monitoring communication through UART.

7\. Understanding the software and hardware structure of a CAN-based embedded

&#x20;  communication system.



\---



\## Technologies Used



\- Embedded C

\- STM32F405

\- ARM Cortex-M4

\- CAN

\- CAN1 / CAN2

\- CAN Interrupts

\- MCP2551

\- UART

\- STM32 HAL

\- STM32CubeIDE

\- STM32CubeMX

\- Git

\- GitHub



\---



\## Applications



\- Embedded automotive communication systems

\- CAN-based distributed control systems

\- Industrial automation

\- Multi-node embedded communication

\- Real-time monitoring and diagnostics

\- ECU-to-ECU communication



\---



\# System Architecture



The overall communication architecture is:



```text

&#x20;                STM32F405

&#x20;             ┌───────────────┐

&#x20;             │               │

&#x20;             │    CAN1/2     │

&#x20;             │  Controller   │

&#x20;             │               │

&#x20;             └───────┬───────┘

&#x20;                     │

&#x20;                     │ CAN TX/RX

&#x20;                     │

&#x20;             ┌───────▼───────┐

&#x20;             │    MCP2551    │

&#x20;             │ CAN Transceiver│

&#x20;             └───────┬───────┘

&#x20;                     │

&#x20;                     │ CANH / CANL

&#x20;                     │

&#x20;                CAN Bus

&#x20;                     │

&#x20;             ┌───────▼───────┐

&#x20;             │ Other CAN Node│

&#x20;             │ / CAN Device  │

&#x20;             └───────────────┘



&#x20;             UART

&#x20;               │

&#x20;               ▼

&#x20;       PC / Serial Monitor

