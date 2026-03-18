# BMCU 27-5

## Product Overview

The BMCU 27-5 is the standard version of the Bidirectional Buffer Module, using mechanical micro-switches for filament detection.

## Firmware Variants

There are two firmware variants for BMCU 27-5:

| Variant | Description |
|---------|-------------|
| **0027** | 4061N's original firmware, perfect Hall effect sub-board, compatible with dual micro-switch sub-board. No special functions such as self-priming. |
| **27** | Stardust's dual micro-switch firmware, perfectly compatible with dual micro-switches, compatible with the original Hall effect. There is a chance to trigger self-priming after photoelectric triggering. |

## Firmware Naming Convention

Format: `[Version]-[Retract Type]`

### Device Identifier

The suffix (A/B/C/D) determines which device the printer recognizes:

- **A** - Device Identifier A
- **B** - Device Identifier B
- **C** - Device Identifier C
- **D** - Device Identifier D

When you flash the firmware, the device identifier is set at that moment, allowing the printer to distinguish between up to 4 devices.

### Retract Types

| Type | Description |
|------|-------------|
| **Discontinuation** | Retracts until filament is no longer present (for dual micro-switches, retracts to middle micro-switch release point), then reverses and feeds back a little bit |
| **Minimum** | Retract distance of 12cm, equivalent to original AMSlite retract distance |
| **XXcm** | Stop after rewinding to XXcm, suitable for different Teflon tube lengths. Note: Due to system response, this unit is not entirely accurate; ruler measurements are for reference only and require manual testing |

### Example

```
BMCU_27-5_A_filament return distance 15cm.bin
│     │  │ │
│     │  │ └── Retract Distance: 15cm
│     │  └──── Device Identifier: A
│     └──────── Version: 27-5
└────────────── Product: BMCU
```


## Compatible Printers

### A1 Series (Tested)
- Bambu Lab A1
- Bambu Lab A1 mini

**Note for A1 Series:**
- Requires firmware version 01.07.xx or higher
- Before connecting BMCU, go to **Printer Settings → AMS Type** and set to **AMS/AMS2 Pro/AMS HT**
- Can recognize up to 4 devices and achieve up to **16-color automatic material changing** printing

### P1 Series (Untested)
- Bambu Lab P1P
- Bambu Lab P1S
- Bambu Lab X1C
- Bambu Lab X1E

**Note for P1 Series:**
- Theoretically works but has not been tested yet

## Firmware Selection

For firmware options, please refer to [Firmware Download List](../Firmware_List/).

## Microswitch Testing

If you are using BMCU 27-5 with micro-switch firmware, you can test if the micro-switch is working properly:

<iframe width="100%" height="400" src="https://www.youtube.com/embed/7Pc5haeAJ8E" frameborder="0" allowfullscreen></iframe>


## Related Documentation

- [LED Status Guide](../LED_Status_Guide)
- [BMCU Burning Tutorial(UART)](../BMCU_Burning_Tutorial(UART).md)
- [Base Bracket STL](../Downloads/Base_Bracket_Print.md)
