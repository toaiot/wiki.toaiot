# BMCU in P series


!!! warning 
    Prior to programming, ensure that.All solder joints are properly finished,No power supply short circuits exist

## Important Notes Before Flashing

### Version Compatibility

- **Before October**: Old version BMCU with dual buffering required different firmware versions; using with P series required flashing firmware
- **After October**: Upgraded dual-microswitch version can be directly plugged in and automatically recognized

> However, the P series with external five-way control requires flashing firmware version 1.08

## Prerequisites

### Tools and Software Required

1. **Dupont wires** - To connect the programmer and BMCU mainboard
2. **USB to UART adapter** - Need to bring your own
3. **Computer** - Windows PC recommended
4. **Software: WCHISPTool** - [Download](./assets/WCHISPTool-v3.3.7z)

## Flashing Steps

### **Step 1**: Hardware Connection

**⚠️ IMPORTANT: Ensure BMCU is NOT connected to the printer!**

Connect the BMCU mainboard and USB-UART tool according to the following wiring:

!\[step1]\(./assets/buring\_tutorial/step1.png null)

### **Step 2**: Install Driver

1. Connect the USB-to-UART tool to your computer
2. The system should automatically detect the serial port
3. Note your specific COM port number (may differ from examples)
4. Use the actual port assigned to your device

!\[step2]\(./assets/buring\_tutorial/step2.png null)

### **Step 3**: Enter Programming Mode

1. **Press and hold** the **B button** with your left hand (do not release)
2. **Press** the **R button** once with your right hand and release
3. **Keep holding** the B button (it's best not to release it)
   !\[step3]\(./assets/buring\_tutorial/step3.png null)

### **Step 4**: Configure WCHISPTool

1. Open WCHISPTool software
2. select the corresponding MCU series, model,download method
3. Check the download configuration
4. Wait for the message: **"(Read/write protection unlocked successfully!)"**

!\[step4]\(./assets/buring\_tutorial/step4.png null)

### **Step 5**: Flash Firmware

1. Click the **"Download"** button
2. Wait patiently for the process to complete

<br/>
#### If download fails:
- Try selecting baud rate of **115200**
- Check Dupont wire connections
- **Note**: The "Contact Protection" button must be clicked for each download attempt

!\[step5]\(./assets/buring\_tutorial/step5.png null)

### **Step 6**: Verify Success

1. **Press the R button** at this point
2. The **red LED** on the BMCU mainboard will illuminate
3. This indicates successful program burning!

