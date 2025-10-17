---
title: Firmware Update and Flashing
description: Complete guide for updating and flashing firmware on your e-paper display devices
---

Before using SenseCraft HMI, it's highly recommended to update your device firmware to the latest version. This ensures optimal performance, bug fixes, and access to the latest features.

## Important Notice

This guide focuses on updating SenseCraft HMI firmware for use with the SenseCraft HMI platform. Keeping your firmware up to date ensures you have access to the latest features, improvements, and bug fixes.

## Firmware Flasher Tool

The Firmware Flasher is an essential tool for keeping your device's software up to date. It provides a simple, step-by-step interface to flash SenseCraft HMI firmware directly from your web browser.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_46.png" style={{width:400, height:'auto'}}/></div>

## Step-by-Step Flashing Guide

### Prerequisites

Before you begin, ensure you have:

- **USB Cable**: Connect your device to your computer
- **Stable Internet**: For downloading firmware files
- **Modern Browser**: Chrome, Firefox, Safari, or Edge recommended
- **Device Power**: Ensure your device has sufficient power

### Step 1: Access the Firmware Flasher

1. Log in to your SenseCraft HMI account
2. Navigate to the **Workspace** tab
3. Click the **Device Flasher** button next to your device

### Step 2: Select Your Device

Before you begin, ensure your device is connected to your computer via a USB cable.

1. Click the **Select** button
2. A modal will appear asking you to choose your device from a list of supported hardware

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_47.png" style={{width:400, height:'auto'}}/></div>

:::note
If you select the **ePaper DIY Kit - EE04**, you will be prompted with an additional step: you must select the specific screen type and size you are using with the kit. This ensures that the correct display drivers are included in the firmware.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_48.png" style={{width:400, height:'auto'}}/></div>
:::

### Step 3: Select Firmware

Once a device is selected, the firmware options will become available.

1. Click the dropdown menu under **Select firmware** to see a list of available SenseCraft HMI firmware versions for your device
2. Choose the version you wish to install:
   - **Latest Version** (Recommended for best performance and latest features)
   - **Previous versions** (if needed for specific compatibility requirements)

**Additional Options:**
- **Connect Serial Monitor**: This button opens a serial monitor in your browser, which is an advanced tool for viewing debug messages and logs from the device during the flashing process

### Step 4: Flash the Firmware

This is the final step where the firmware is written to the device.

1. Click the **Flash** button to begin the process
2. **Important**: Do not disconnect the device or close the browser tab until the process is complete
3. The tool will show a progress bar indicating the status of the flash

:::tip
You will see a checkbox labeled **Full Flash**. Be very careful with this option:

**Standard Flash (unchecked)**:
- Updates the firmware but preserves your saved settings
- Keeps Wi-Fi credentials and device configuration
- Recommended for regular updates

**Full Flash (checked)**:
- Erases the **entire** flash memory on the device
- **This will delete all saved settings, including your Wi-Fi password**
- You will need to reconfigure your Wi-Fi connection after a Full Flash
- Recommended for troubleshooting, performing a "factory reset", or when experiencing persistent issues
:::

## After Flashing

### First Boot
1. Wait for the device to restart automatically
2. The device will boot with the new firmware
3. Check the device display for any error messages

### Next Steps - Device Setup

After successfully flashing the SenseCraft HMI firmware, you'll need to set up your device for first-time use. Follow the device-specific guides below:

**For reTerminal E1001:**
- Complete setup guide: [Getting Started with reTerminal E1001 - Network Setup](https://wiki.seeedstudio.com/getting_started_with_reterminal_e1001/#network-setup)

**For reTerminal E1002:**
- Complete setup guide: [Getting Started with reTerminal E1002 - Network Setup](https://wiki.seeedstudio.com/getting_started_with_reterminal_e1002/#network-setup)

These guides will walk you through:
- Powering on your device
- Connecting to Wi-Fi
- Pairing with the SenseCraft HMI platform
- Creating your first dashboard

### Reconfiguration (if Full Flash was used)
If you performed a Full Flash, you'll need to:
1. **Reconnect to Wi-Fi**: Set up your network connection again
2. **Reconnect to Platform**: Re-add the device to your SenseCraft HMI account
3. **Restore Settings**: Reconfigure any custom settings

## Troubleshooting

### Common Issues

**Device Not Detected**
- Ensure USB cable is properly connected
- Try a different USB port
- Check if device drivers are installed
- Restart your browser

**Flashing Failed**
- Don't disconnect the device during flashing
- Ensure stable internet connection
- Try using a different browser
- Check device power level

**Device Won't Boot After Flash**
- Wait a few minutes for the device to initialize
- Try a Full Flash if you used Standard Flash
- Check the serial monitor for error messages
- Contact support if problems persist

**Wi-Fi Connection Lost**
- This is normal after a Full Flash
- Reconfigure Wi-Fi settings on the device
- Re-add the device to your platform account

### Getting Help

- **Serial Monitor**: Use the built-in serial monitor to view debug information
- **Documentation**: Check other guides for specific issues
- **Community Forum**: [Seeed Studio Forum](https://forum.seeedstudio.com/)
- **Support**: Contact technical support (techsupport@seeed.io)


## Best Practices

### Before Flashing
- **Backup Settings**: Note down important device settings
- **Stable Environment**: Ensure stable power and internet
- **Close Other Applications**: Free up system resources

### During Flashing
- **Don't Interrupt**: Never disconnect or close browser during flashing
- **Monitor Progress**: Watch the progress bar and any status messages
- **Be Patient**: Flashing can take several minutes

### After Flashing
- **Test Functionality**: Verify all features work correctly
- **Update Platform**: Ensure you're using the latest platform version
- **Document Changes**: Keep track of firmware versions for troubleshooting

---

*Ready to start using your updated device? Check out our [Workspace Interface Guide](/guides/workspace-interface/) to learn how to create your first project.*
