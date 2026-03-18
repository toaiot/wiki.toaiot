# LED Status Guide

## Overview

The BMCU uses WS2812 RGB LEDs for status indication. The lighting system is divided into two parts:

| System              | LED Count               | Location     |
| ------------------- | ----------------------- | ------------ |
| SystemStatusLight   | 1                       | Main board   |
| ChannelStatusLights | 2 per channel (8 total) | Each channel |

***

## Channel Status Light (MC_STU_RGB_set)

Located at Channel Light 1 (near the buffer), this indicates the channel status:

<table style="width:100%;">
  <thead>
    <tr>
      <th style="width:180px;text-align:left;">Color</th>
      <th style="text-align:left;">Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#00FF00;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Green</strong></td>
      <td>The channel is feeding material (send_out)</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#800080;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Purple</strong></td>
      <td>The channel is pulling back material (pull_back)</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#FFFFFF;border:1px solid #ccc;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>White</strong></td>
      <td>The channel is in use (on_use)</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#90EE90;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Light Green</strong></td>
      <td>The consumable material is detected by the tool head and is being bitten</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#FFA500;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Orange/Gold</strong></td>
      <td>Only the external micro-switch is triggered</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#00FFFF;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Cyan</strong></td>
      <td>Only the internal micro-switch is triggered</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#000000;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Black</strong></td>
      <td>The system is offline and no consumable material is triggered</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#0080FF;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Blue</strong></td>
      <td>The channel is in idle state (idle); the system will not distinguish whether there is consumable material when online</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#FF0000;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Red ❌</strong></td>
      <td>AS5600 communication failed or the radial magnet of AS5600 does not exist, the channel is locked</td>
    </tr>
  </tbody>
</table>

***

## Buffer Status Light (MC_PULL_ONLINE_RGB_set)

Located at Channel Light 2 (near the gear), this indicates the buffer status:

<table style="width:100%;">
  <thead>
    <tr>
      <th style="width:180px;text-align:left;">Color</th>
      <th style="text-align:left;">Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#FF0000;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Red</strong></td>
      <td>Excessive pressure (triggers auxiliary feeding when allowed)</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#0080FF;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Blue</strong></td>
      <td>Insufficient pressure (triggers auxiliary material pull-back when allowed)</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#808080;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Off</strong></td>
      <td>No filament or normal pressure but no micro-switch trigger</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:transparent;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Set according to<br/>consumable material color<br/>(off when black)</strong></td>
      <td>Normal pressure, both micro-switches triggered</td>
    </tr>
  </tbody>
</table>


***

## System Status Light

The main system status indicator:

<table style="width:100%;">
  <thead>
    <tr>
      <th style="width:180px;text-align:left;">Color</th>
      <th style="text-align:left;">Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#FFFFFF;border:1px solid #ccc;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Bright White</strong></td>
      <td>System initializing (startup)</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#FF6B6B;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Light Red</strong></td>
      <td>System offline (error state)</td>
    </tr>
    <tr>
      <td style="display:flex;align-items:center;white-space:nowrap;"><span style="display:inline-block;width:12px;height:12px;background-color:#F0F0F0;border-radius:50%;margin-right:8px;flex-shrink:0;"></span><strong>Light White</strong></td>
      <td>System online (normal working state)</td>
    </tr>
  </tbody>
</table>

***

## Quick Reference

### Normal Operation

- System Status: Light White (Online)
- Channel Status: Blue (Idle) or Green/Purple (Active)

### Warning Signs

- Channel Status: Orange/Gold or Cyan (Check micro-switches)
- Buffer Status: Red (Excessive pressure) or Blue (Insufficient pressure)

### Error States

- Channel Status: Red (AS5600 error, channel locked)
- System Status: Light Red (System offline)

