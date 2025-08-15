# D22 - Chipster

This document provides the pinout and description for the D-22 Chipster, a 3-qubit Quantum Fourier Transform (QFT) chip.

## Current Progress
| Criteria | Description | Status |
| :--- | :--- | :--- |
| Floorplan or Die Size Area | 0.665 mm x 0.683 mm | PASSED |
| Antenna Violation | 6 (need diode insertion) | ALMOST |
| Static Timing Analysis | Only Max Cap and Max Slew errors | ALMOST |
| DRC Errors | 0 | PASSED |
| LVS | Matched | PASSED |
| Num of Pins | 197 (Need to be serialized) | ALMOST |

## Pad Rings + GDS
The detailed link of pad rings + GDS : https://docs.google.com/presentation/d/1Jy2QJi_8KYM8i0dF_CQpoXG_GRtNdFFhPNUrgbnHmIE/edit?slide=id.g37506a79484_0_80#slide=id.g37506a79484_0_80

## Pin List & Description

The following table details the signals for the module based on the Verilog definition and required power supplies.
The detailed link of pin list : https://docs.google.com/spreadsheets/d/1T-fU9Hze27ewmNjL59FZzfohovZzRloE966pTiVe4rU/edit?usp=sharing

| Pin Name | Direction | Description |
| :--- | :--- | :--- |
| `clk` | Input | System clock signal. |
| `rst_n` | Input | Active-low reset signal. |
| `i000_r`, `i000_i` | Input | Real and imaginary parts of the initial state vector component α000. |
| `i001_r`, `i001_i` | Input | Real and imaginary parts of the initial state vector component α001. |
| `i010_r`, `i010_i` | Input | Real and imaginary parts of the initial state vector component α010. |
| `i011_r`, `i011_i` | Input | Real and imaginary parts of the initial state vector component α011. |
| `i100_r`, `i100_i` | Input | Real and imaginary parts of the initial state vector component α100. |
| `i101_r`, `i101_i` | Input | Real and imaginary parts of the initial state vector component α101. |
| `i110_r`, `i110_i` | Input | Real and imaginary parts of the initial state vector component α110. |
| `i111_r`, `i111_i` | Input | Real and imaginary parts of the initial state vector component α111. |
| `f000_r`, `f000_i` | Output | Real and imaginary parts of the final state vector component ψ000. |
| `f001_r`, `f001_i` | Output | Real and imaginary parts of the final state vector component ψ001. |
| `f010_r`, `f010_i` | Output | Real and imaginary parts of the final state vector component ψ010. |
| `f011_r`, `f011_i` | Output | Real and imaginary parts of the final state vector component ψ011. |
| `f100_r`, `f100_i` | Output | Real and imaginary parts of the final state vector component ψ100. |
| `f101_r`, `f101_i` | Output | Real and imaginary parts of the final state vector component ψ101. |
| `f110_r`, `f110_i` | Output | Real and imaginary parts of the final state vector component ψ110. |
| `f111_r`, `f111_i` | Output | Real and imaginary parts of the final state vector component ψ111. |
| `VCC` | Power | 5V Power Supply. |
| `VDD` | Power | 3.3V Power Supply. |
| `VSS` | Ground | Ground connection. |

## Pin Count Summary

* **Input Pins:** **18** (`clk`, `rst_n`, and 16 state vector inputs (WIDTH = 6))
* **Output Pins:** **16** (16 state vector outputs (WIDTH = 6))
* **Power/Ground Pins:** **3** (`VCC`, `VDD`, `VSS`)
* **Total Pins:** **37**

Probably serial to parallel or UART or SPI is needed in order to reduce the number of pins, because likely the calculation is 32 * 6 + 5 = 197 ?
