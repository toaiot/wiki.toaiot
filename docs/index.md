# BMCU Product Documentation

Welcome to the Toaiot BMCU product documentation center. Here you will find firmware, user manuals, 3D models, and tutorials for BMCU (Bidirectional Buffer Module) products.

## What is BMCU?

BMCU (Bidirectional Buffer Module) is a filament buffer system designed for 3D printers. It helps manage multi-color printing and AMS auto-feed systems by providing intelligent filament buffering and switching.

### Key Features

- Automatic filament switching
- Support for multiple channels (A, B, C, D)
- Real-time status indication via RGB LEDs
- Compatible with Bambu Lab printers

## Product Versions

| Version   | Detection Method          | Firmware     |
| --------- | ------------------------- | ------------ |
| BMCU 27-5 | Mechanical Micro-switch   | Version 0027 |
| BMCU 370C | Hall Sensor (Contactless) | Version 0020 |

### BMCU 27-5

The standard version using mechanical micro-switches for filament detection. Suitable for most users.

[BMCU 27-5 Details](./BMCU_27-5/)

### BMCU 370C

The advanced version using Hall sensor technology for contactless detection. No mechanical wear, more precise.

[BMCU 370C Details](./BMCU_370C/)

## Quick Start

### Step 1: Choose Your Version

- **Standard**: BMCU 27-5 (mechanical micro-switch)
- **Advanced**: BMCU 370C (Hall sensor)

### Step 2: Select Firmware

Choose firmware based on:

- Hardware version (27-5 or 370C)
- Channel position (A, B, C, D)
- Filament return distance (15cm recommended)

[Firmware Download List](./Firmware_List/)

### Step 3: Install

1. Print the base bracket (if needed)
2. Mount BMCU to your printer
3. Flash the appropriate firmware
4. Configure and test

## Guides

- [LED Status Guide](./LED_Status_Guide) - Understand LED indicators
- [BMCU Burning Tutorial(UART)](./BMCU_Burning_Tutorial\(UART\).md) - How to flash firmware
- [Base Bracket STL](./Base_Bracket_Print) - Download 3D models

## LED Status Quick Reference

| Status         | Color       | Meaning             |
| -------------- | ----------- | ------------------- |
| System Online  | Light White | Normal operation    |
| System Offline | Light Red   | Error state         |
| Feeding        | Green       | Sending filament    |
| Pulling Back   | Purple      | Retracting filament |
| Idle           | Blue        | Waiting             |

For detailed LED status information, see the [LED Status Guide](./LED_Status_Guide).

## Compatible Printers

- Bambu Lab P1P
- Bambu Lab P1S
- Bambu Lab X1C
- Bambu Lab X1E
- Bambu Lab A1 (with base bracket)
- Bambu Lab A1 mini (with base bracket)


## Technical Support

For additional support, please contact FYSETC or visit the official documentation.
