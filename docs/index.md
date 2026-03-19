# What is BMCU?

## Introduction
---
**BMCU (Bidirectional Buffer Module)** is a filament buffer system designed for 3D printers. It helps manage multi-color printing and AMS auto-feed systems by providing intelligent filament buffering and switching.

BMCU operates on a **four-channel unit** and is currently designed with the **CH32 microcontroller** as the main control unit.

!!! warning 
    BMCU is intended only for DIY learning and can be integrated with **A1, A1mini, and P1 Series printers** for operation.

Its functions are **similar to AMS lite**, primarily enabling **multi-material printing and automated feeding**. However, it **does not support RFID material recognition**.

## Features
---
1. **Faster Filament Switching** – No need to retract to break detection; simply exit the five-way valve for quicker material changes.
2. **Compact Side-by-Side Design** – No built-in spool holder, allowing filaments to be stored in sealed dry boxes.
3. **Active Buffer System** – Pre-feeds filament before the printer requests it, reducing resistance and preventing feeding issues.
4. **Standardized Components** – Uniform part parameters improve DIY success rates and lower costs.
5. **Photoelectric Detection** – Detects transparent filaments without contact, eliminating mechanical resistance and instability.