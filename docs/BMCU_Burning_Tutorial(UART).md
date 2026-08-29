# BMCU Burning Tutorial(UART)

# BMCU 370C V2.0
**⚠️ This tutorial only applies to versions with a Type-C interface**
!\[1787910661634]\((https://github.com/toaiot/wiki.toaiot/blob/main/docs/assets/buring_tutorial/1787910661634.png?raw=true))

## Prerequisites

1. **Type-C：**USB to Type-C
2. **Computer：**Windows PC recommended
3. **Software: BMCU Flasher** - [Download](https://github.com/toaiot/BMCU-Flasher/releases/tag/v1.3-toaiot-native-usb) )

## Flashing Steps

### **Step 1**: Hardware Connection 

**⚠️ IMPORTANT: Ensure BMCU is NOT connected to the printer!** 

Connect the BMCU mainboard and Computer according to the following wiring:
!\[1787911652753]\((https://github.com/toaiot/wiki.toaiot/blob/main/docs/assets/buring_tutorial/1787911652753.png?raw=true))

### **Step 2**: Install Driver 

1. Install the **BMCU Flasher** program and open it
!\[1787912271982]\(./assets/buring_tutorial/1787912271982.png)
!\[1787912271983]\(./assets/buring_tutorial/1787912271983.png)

2. Click **ONative USB (manual BOOT+RESET)**, and the system should automatically detect the serial port
!\[1787912271984]\(./assets/buring_tutorial/1787912271984.png)


3. Click **Online**, keep the default selection in the pop-up window, and then click **Select**
!\[1787912271985]\(./assets/buring_tutorial/1787912271985.png)
!\[1787912271986]\(./assets/buring_tutorial/1787912271986.png)

4. Click **Flash** and wait for the flashing process to complete
!\[1787912271987]\(./assets/buring_tutorial/1787912271987.png)

5. Flashing complete
**⚠️ After flashing, plug the BMCU into the printer; the BMCU will automatically perform a channel calibration that takes about 4 minutes** 
!\[1787912271988]\(./assets/buring_tutorial/1787912271988.png)

   5.1 If the following message appears when clicking Flash: **identify failed (native usb).enter bootloader first. last=native usb: no WCH ISP USB device (4348:55E0).enter bootloader first (hold BOOT + tap RESET), and check driver: windows = WCH CH375 driver (CH375DLL64.dll) or WinUsB via Zadig, Linux = udev rules + libusb**
   !\[1787912271989]\(./assets/buring_tutorial/1787912271989.png)

   5.2 You need to install the **TP-ISPTool driver** - [Download](https://github.com/toaiot/BMCU-Flasher/releases/tag/v1.3-toaiot-native-usb) )
   !\[1787912271990]\(./assets/buring_tutorial/1787912271990.png)
   !\[1787912271991]\(./assets/buring_tutorial/1787912271991.png)

   5.3 Close the **BMCU Flasher** program and reopen it, unplug and replug the connection cable between the BMCU and the computer, then repeat the flashing steps above;
   !\[1787912271988]\(./assets/buring_tutorial/1787912271988.png)



# BMCU 370C V1.0
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

!\[step1]\(./assets/buring_tutorial/step1.png)

### **Step 2**: Install Driver

1. Connect the USB-to-UART tool to your computer
2. The system should automatically detect the serial port
3. Note your specific COM port number (may differ from examples)
4. Use the actual port assigned to your device

!\[step2]\(./assets/buring_tutorial/step2.png)

### **Step 3**: Enter Programming Mode

1. **Press and hold** the **B button** with your left hand (do not release)
2. **Press** the **R button** once with your right hand and release
3. **Keep holding** the B button (it's best not to release it)
   !\[step3]\(./assets/burning_tutorial/step3.png)

### **Step 4**: Configure WCHISPTool

1. Open WCHISPTool software
2. select the corresponding MCU series, model,download method
3. Check the download configuration
4. Wait for the message: **"(Read/write protection unlocked successfully!)"**

!\[step4]\(./assets/burning_tutorial/step4.png)

### **Step 5**: Flash Firmware

1. Click the **"Download"** button
2. Wait patiently for the process to complete

<br/>
#### If download fails:
- Try selecting baud rate of **115200**
- Check Dupont wire connections
- **Note**: The "Contact Protection" button must be clicked for each download attempt

!\[step5]\(./assets/burning_tutorial/step5.png)

### **Step 6**: Verify Success

1. **Press the R button** at this point
2. The **red LED** on the BMCU mainboard will illuminate
3. This indicates successful program burning!

