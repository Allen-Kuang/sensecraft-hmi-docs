---
title: Deploying to Your Device
description: Complete guide for deploying your SenseCraft HMI projects to your e-paper display devices
---

Once you've created your content using any of the SenseCraft HMI functions (Dashboard, Gallery, Canvas, RSS, or Web), you'll want to deploy it to your Seeed device. This guide covers the deployment process for all content types.

## Preview Before Deployment

Before deploying your content to the device, it's important to preview how it will look:

Step 1. Click the "Preview" button in the top toolbar

Step 2. Review how your layout will appear on the device

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_24.png" style={{width:400, height:'auto'}}/></div>

Step 3. Make any necessary adjustments to your design

:::tip
The preview function allows you to see exactly how your content will appear on the device screen, helping you identify any layout issues before deployment.
:::

## Save Your Layout

Before deploying, make sure to save your work:

Step 1. Click the "Save" button to store your current layout

Step 2. Your layout will be saved to the SenseCraft HMI cloud

:::note
Saving your layout ensures that your work is preserved and can be accessed from any device or browser.
:::

## Deploy to Device

Once you're satisfied with your preview and have saved your layout:

Step 1. Ensure your device is connected and shows "Online" status

Step 2. Click the "Deploy" button

Step 3. Wait for the deployment process to complete

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_25.png" style={{width:400, height:'auto'}}/></div>

Step 4. Your layout will appear on your connected device

## Deployment Considerations

For successful deployment to Seeed devices, consider the following:

### 1. Device Compatibility
- Ensure your layout is optimized for your specific device's screen resolution
- Different devices have different screen sizes and capabilities
- Test your layout on the target device's resolution

### 2. Connection Status
- Make sure your device shows "Online" status before deploying
- Check that your device is properly connected to the internet
- Verify the device is paired with your SenseCraft HMI account

### 3. Data Components
- If using data components (Weather, Stock, etc.), ensure your device has internet connectivity
- Some data sources may require API keys or authentication
- Check that all external data sources are accessible

### 4. Device Sensors
- Components like Battery, Temperature, and Humidity will only work with compatible Seeed reTerminal E Series ePaper Display devices that have the appropriate sensors
- Verify that your device has the required hardware for sensor-based components

### 5. Refresh Rate
- Set an appropriate interval time based on how frequently your data needs updating and your device's capabilities
- Consider battery life when setting refresh intervals
- Balance between data freshness and power consumption

---

**Congratulations!** You've successfully deployed your content to your device. Your e-paper display should now show your custom layout.

*Need help with specific functions? Check out our detailed guides for [Workspace Interface](/guides/workspace-interface/), [Gallery](/guides/sensecraft-hmi-gallery/), [Canvas](/guides/sensecraft-hmi-canvas/), [RSS](/guides/sensecraft-hmi-rss/), and [Web](/guides/sensecraft-hmi-web/) functions.*
