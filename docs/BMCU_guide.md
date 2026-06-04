## Download BMCU-Flasher and BambuStudio-BMCU.

Download BMCU-Flasher here: [BMCU-Flasher](https://github.com/jarczakpawel/BMCU-Flasher/releases/tag/v1.3)

## Launch BMCU-Flasher

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/BMCU-Flasher.png" width="800">
</p>

## Update Firmware

#### Remove the screws and detach the enclosure

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/screw.png" width="800">
</p>

#### Connect the PC to the BMCU using a USB-to-TTL adapter

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/help.png" width="800">
</p>

#### Set BMCU Flasher

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/set.png" width="800">
</p>

#### Select fireware

Click "Online" to open the firmware selection window.
<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/fireware.png" width="800">
</p>

Click "Browse" to open the firmware selection window, then choose the local firmware to flash. The firmware can be downloaded from:
https://github.com/jarczakpawel/BMCU-C-PJARCZAK/releases/tag/V10.5.
The firmware package contains firmware specifically for the P1S, and the A1 firmware can be used on A1 and P2S devices.

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/localfireware.png" width="800">
</p>


Filament Load Force Notes:

Select ‘High Force’ for the P1S, and ‘Standard Force’ for all other machines.


BMCU Slot Notes:

Select AMS_A. If using multiple BMCUs, assign AMS_B, AMS_C, and AMS_D to the additional BMCUs in sequential order.


Retraction Description:

This setting is used to specify the retraction distance for the filament after it has been cut during the material change process. Once the filament retraction is complete, the new filament will be fed into the extruder from a different BMCU slot.

#### Flash

Click "Flash" to begin flashing the firmware. When prompted by the software, press and hold the Boot button, then click the Reset button.
<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/button.png" width="800">
</p>

Once the flashing process is complete, reinstall the enclosure screws.

## Calibration

#### Install all four connectors

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/connector.png" width="800">
</p>

#### Turn off the machine's power

Do not plug or unplug any connection wires on the printed circuit board when the printer is turned on.

#### Connect Machine and BMCU

When connecting the cable between the machine and the BMCU, please pay attention to the insertion direction of the cable.
<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/connect.png" width="800">
</p>


#### Turn on the machine's power

#### Calibrate slot 1

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/light.png" width="800">
</p>

When the BMCU is powered on, LEDs 1–4 will flash briefly and then stop. When LED 1 starts flashing blue, press Plug 1 downward and hold for about one second, then release; LED 1 will then flash red. After two seconds, pull Plug 1 upward and hold for about one second, then release. Once LED 2 begins to flash blue, the calibration for Channel 1 is complete, and you may proceed to calibrate Channel 2.

#### Calibrate other slot

The calibration steps for the other channels are the same as for Channel 1. When the channel’s blue LED starts flashing, press the plug and release it, then pull the plug upward.

Once Channel 1 calibration is complete, Indicator 2 will start flashing blue, signaling that Channel 2 can be calibrated. After Channel 2 calibration is finished, Indicator 3 will flash blue, allowing calibration of Channel 3. When Channel 3 calibration is complete, Indicator 4 will flash blue, enabling calibration of Channel 4. After all four channels have been calibrated and Indicators 1–8 have flashed, Indicators 1–4 will remain steadily lit.

#### Check Calibration

Press and release the plug for a channel. The channel’s two LEDs will light up, and the internal motor will start rotating. Pull the plug upward and release it; the LEDs will turn red, and the motor will rotate again. Verify that all four channels display the same behavior.

## Installation and Feeding

#### Installation

Use the 4-in-1 adapter and PTFE tube to connect the machine to the BMCU.
<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/install.png" width="800">
</p>

#### Feeding

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/feed.png" width="800">
</p>

Once the filament is inserted into the feed port, the BMCU will automatically load the filament.

## Print

#### Printer Firmware

The Bambu Lab P1S (firmware version 01.08.00.00), A1 (firmware version 01.08.00.00), and P2S (firmware version 01.01.03.00) printers support normal printing.

#### Launch the BambuStudio

#### Connect Device

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/device.png" width="800">
</p>

#### Modify Slot Information

Each slot must be loaded with material first; otherwise, the  information will not be displayed or editable.
<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/filament.png" width="800">
</p>

When multiple BMCUs are used, switch between the different BMCUs to configure all available slots.
<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/BMCU.png" width="800">
</p>

#### Slice Model

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/Slice.png" width="800">
</p>

#### Print Model

<p align="center">
  <img src="../assets/BMCU_Debug_and_Usage_Guide/print.png" width="800">
</p>

