# Modular I2C GPIO Expander / Power Switch Board (Qwiic-Compatible)

A compact, Qwiic-compatible power switch module built around an I2C GPIO expander, designed for easy integration into modular sensor/electronics setups without extra wiring or a microcontroller doing the switching directly.

![PCB Top View](images/pcb-top.png)
![Schematic]([images/schematic.pn](https://github.com/Harshad-vali/QWIIC-SWITCH-PROJECT/blob/e31072e05f0342936bdecb25705b8014027564fc/Screenshot%202026-05-05%20202835.png)g)

## Overview

This board lets a host microcontroller switch power to a downstream load over I2C, using a GPIO expander instead of dedicated GPIO pins. It's designed to snap into the Qwiic ecosystem, so it can be daisy-chained with other Qwiic boards with no soldering.

## Key Features

- **I2C-controlled power switching** using the PCA9536 GPIO expander
- **PCA9306 I2C level shifter** for safe voltage-level translation between 3.3V and 5V I2C buses
- **Impedance-controlled I2C routing** to keep signal integrity clean on the bus
- **MOSFET switching circuitry** for the actual load power path
- **Status LED indicators** showing real-time switch state at a glance
- **Qwiic-compatible connectors** for plug-and-play integration with other boards

## Design Details

- Schematic capture and PCB layout done fully in KiCad
- Routed with attention to I2C trace impedance to avoid signal integrity issues on the bus
- Component placement optimized for a compact footprint
- Manufacturing-ready output: complete BOM, Gerber files, and drill files generated for fabrication

## Tools Used

- KiCad (schematic capture + PCB layout)

## Files in This Repo

- `schematic.pdf` — full schematic
- `pcb-layout/` — top/bottom copper and layer images
- `gerbers/` — manufacturing files (if included)
- `BOM.csv` — bill of materials with supplier part numbers

## What I'd Improve Next

- Add reverse-polarity protection on the input
- Explore a smaller PCA9536 package option to shrink the footprint further

---
*Part of a PCB design training program (SUREPROED). Designed and routed independently as part of the coursework.*
