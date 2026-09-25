# Modular I2C GPIO Expander / Power Switch Board (Qwiic-Compatible)

A compact, Qwiic-compatible power switch module built around an I2C GPIO expander, designed for easy integration into modular sensor/electronics setups without extra wiring or a microcontroller doing the switching directly.

![3D Front View](https://github.com/Harshad-vali/QWIIC-SWITCH-PROJECT/blob/90c395c93afc004e473f713c59a727cddb5dd03d/3D%20front%20layer.png)
![3D Back View](3D%20back%20layer.png)
![3D Side View](3D%20side%20view.png)

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

### Copper Layers

![All Copper Layers](all%20cu%20layers.png)
![Front Copper Layer](front%20cu%20layer.png)
![Back Copper Layer](back%20cu%20layer.png)

### Assembly Layers

![Front Assembly Layer](front%20assemble%20layer.png)
![Back Assembly Layer](back%20assemble%20layer.png)

### Schematic

![Schematic Preview](https://github.com/Harshad-vali/QWIIC-SWITCH-PROJECT/blob/5663c37b24583427fa52ad9113f4379495854d5c/schmatic.png)

Full schematic PDF: [Qwiic_Power_Switch_Schematic_v10.pdf](Qwiic_Power_Switch_Schematic_v10%20(1).pdf)

## Tools Used

- KiCad (schematic capture + PCB layout)

## Files in This Repo

- `power switch.kicad_sch` / `power switch.kicad_pcb` / `power switch.kicad_pro` — full KiCad project
- `Qwiic_Power_Switch_Schematic_v10 (1).pdf` — full schematic
- `3D front layer.png`, `3D back layer.png`, `3D side view.png` — 3D renders
- `front cu layer.png`, `back cu layer.png`, `all cu layers.png` — copper layer views
- `front assemble layer.png`, `back assemble layer.png` — assembly drawings
- `schematic.png` — schematic preview image
- `power switch proj 3 main bom.xlsx` — bill of materials with supplier part numbers

## What I'd Improve Next

- Add reverse-polarity protection on the input
- Explore a smaller PCA9536 package option to shrink the footprint further

---
*Part of a PCB design training program (SUREPROED). Designed and routed independently as part of the coursework.*
