# Qualcomm Board Validation Advanced Modular Simulation Project

![C](https://img.shields.io/badge/C-Low_Level_Drivers-blue)
![C++](https://img.shields.io/badge/C++-Simulation_Logic-orange)
![Python](https://img.shields.io/badge/Python-Automation_&_Dashboard-green)
![Embedded](https://img.shields.io/badge/Embedded-Qualcomm_Workflow-purple)
![Status](https://img.shields.io/badge/Status-Active_Development-success)

A modular Qualcomm board validation and simulation framework designed to model embedded hardware bring-up, driver validation, and automated testing workflows.

---

## Overview

This project combines **C**, **C++**, and **Python** to simulate realistic embedded software development environments and board validation workflows.

### Technology Stack

| Language | Purpose                                                 |
| -------- | ------------------------------------------------------- |
| C        | Low-level hardware drivers                              |
| C++      | Device abstraction and simulation engines               |
| Python   | Automation, dashboards, logging, and test orchestration |

---

## Architecture Flow

```text
Boot Sequence
      │
      ▼
Peripheral Initialization
      │
      ▼
Driver Layer Bring-up
 ├── PMIC ADC / Thermistor
 ├── USB Host / Device
 ├── CAN Bus
 ├── SD Card
 ├── LED Control
 └── INA231 Power Monitor
      │
      ▼
Simulation Engine
 ├── Sensor Simulation
 ├── Event Injection
 ├── Dashboard Rendering
 └── Log Collection
      │
      ▼
Automated Testing
 ├── Unit Tests
 ├── Integration Tests
 └── Regression Tests
      │
      ▼
Reports & Outputs
```

---

## Features

* Modular embedded driver architecture
* PMIC ADC multi-channel simulation
* Thermistor monitoring
* USB hotplug and enumeration simulation
* CAN traffic generator and loopback validation
* SD card insertion/removal and filesystem simulation
* LED blink pattern and PWM simulation
* INA231 voltage, current, and power monitoring
* Virtual dashboard console output
* Automated test execution and reporting

---

## Example Virtual Output

<p align="center">
  <img src="docs/images/qualcomm_virtual_dashboard.png" alt="Qualcomm Board Virtual Dashboard" width="100%">
</p>

```text
[BOOT] Qualcomm board initialized
[USB] Device connected -> enumeration success
[SD] Card inserted -> mounted /dev/mmcblk0p1
[CAN] RX Frames/sec = 142
[PMIC] ADC0=3.31V ADC1=1.81V TEMP=36.4C
[INA231] Voltage=5.02V Current=0.43A Power=2.16W
[LED] Blink pattern HEARTBEAT active
```

---

## Build & Run

### Build All Modules

```bash
./scripts/build_all.sh
```

### Run Simulation

```bash
./scripts/run_simulation.sh
```

### Execute Tests

```bash
./scripts/run_tests.sh
```

---

## Repository Structure

```text
Qualcomm_Board_Validation/
│
├── drivers/          Embedded peripheral drivers
├── simulation/       Virtual hardware and dashboard modules
├── tests/            Unit, integration, and regression tests
├── outputs/          Logs, reports, and generated artifacts
├── docs/             Architecture and learning documentation
└── scripts/          Build and execution scripts
```

---

## Learning Outcomes

* Embedded driver lifecycle understanding
* Qualcomm board bring-up concepts
* Hardware abstraction layer (HAL) design
* Event-driven and interrupt-based architectures
* Validation automation workflows
* Multi-language embedded project organization

---

## Future Improvements

* UART console simulator
* I2C transaction viewer
* SPI peripheral simulation
* Linux DTS parser
* Interactive web dashboard

---


