---
description: A comprehensive guide to getting started with the HMI Platform, covering template selection, workspace management, device pairing, and advanced tools.
title: Getting Started with HMI Platform
keywords:
  - HMI Platform
  - E-ink Display
  - Workspace Management
  - Firmware Flashing
  - Image Dithering
last_update:
  date: 1/9/2026
  author: Allen
---

## Introduction

Welcome to the **HMI Platform**, a powerful and user-friendly interface designed to manage and customize your E-ink display devices. This platform serves as the central hub where you can explore creative templates, design your own dashboards, manage device settings, and optimize images for E-ink technology.

Whether you want to display a simple calendar, track stock markets, or create a personalized photo album, the HMI Platform streamlines the process from design to deployment.


## Home Page: Exploring Templates

The **Home Page** is your starting point for creativity. It features a diverse collection of templates, ranging from monochromatic styles to colorful designs suitable for various E-ink displays.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/home.jpg" style={{width:1000, height:'auto'}}/></div>

**Step 1.** Browse the template gallery. We currently offer more than **30+ templates** covering various scenarios such as:
*   **Productivity**: Google Calendar, Github Tracker
*   **Lifestyle**: Weather Station, Days Matter
*   **Finance**: Stock Dashboard

**Step 2.** Select a template that interests you. Once clicked, the template will automatically load into your personal **Workspace**.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/workspace.jpg" style={{width:800, height:'auto'}}/></div>

**Step 3.** In the Workspace, you can modify the template to suit your preferences (e.g., changing location for weather, adding personal events).

**Step 4.** Click the **Save** button in the top right corner to store the customized template in your personal library.

**Step 5.** Click the **Apply** button in the top right corner to apply this page into your device.

## Workspace: Designing Your Content

The **Workspace** is your personal design studio. Here, you manage all your creative assets and organize how they appear on your device.


<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/workspace2.jpg" style={{width:800, height:'auto'}}/></div>

### Creating Content
You can create a new page to design custom layouts including:
- **Design Elements**: Basic shapes and text.
- **Images**: Upload personal photos.
- **RSS Feeds**: Display news or blog updates.
- **Web Content**: Embed web-based information.

### Organizing Playlists
You can combine multiple pages into a **Playlist** or **Album**. When synchronized to the device, these pages will rotate automatically based on the device's interval settings.

## Device: Management and Settings

The **Device** page is the command center for your hardware. It allows you to bind new devices and configure their behavior.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/device.jpg" style={{width:800, height:'auto'}}/></div>

### Pairing a New Device

**Step 1.** Click the **New Device** button.<Br/>
**Step 2.** Enter the **Pairing Code** displayed on your E-ink device screen.<Br/>
**Step 3.** Once verified, the device will be bound to your account and appear in the device list.

### Device Configuration

Click on a specific device to access its detailed settings page. Here you can manage the content queue and view status indicators.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/device2.jpg" style={{width:800, height:'auto'}}/></div>

#### Top Bar Indicators
- **Battery Level**: Shows the current power status of the device.
- **Interval Time**: Sets the duration a page is displayed before switching to the next one (or before the device goes back to sleep).

#### Operation Modes
The platform supports two primary modes, which can be toggled via the top bar:

1.  **Always On Mode**:
    - The device remains active and does not enter sleep mode.
    - **Best for**: Debugging, real-time updates, or when testing new designs.
    - *Note: This mode consumes more power.*

2.  **Sleep Mode**:
    - The device wakes up periodically based on the **Interval Time**, updates the display, and then returns to deep sleep.
    - **Best for**: Daily use.
    - **Benefit**: Extremely power-efficient. Depending on the interval settings, the device can last approximately **3 months** on a single charge.

## Tools: Advanced Utilities

The **Tools** section provides essential utilities for firmware management and image processing.

### Firmware Flashing

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/tools.jpg" style={{width:800, height:'auto'}}/></div>

Our devices come pre-loaded with the standard HMI firmware. However, if you have experimented with third-party firmware (such as Home Assistant or Arduino) and wish to revert to the original factory state, use this tool.

- **Full Flash**: Use this when reverting from a different firmware (e.g., Arduino/ESPHome) back to the HMI firmware. This performs a complete wipe and rewrite.
- **Standard Update**: If you are simply upgrading the HMI firmware version (e.g., from v1.0.7 to v1.0.8), a Full Flash is not required. The standard update is faster.

### Image Dithering

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/dithering.jpg" style={{width:800, height:'auto'}}/></div>

E-ink screens typically have limited color palettes (often just black and white, or limited grayscale). Displaying a standard photograph directly can result in "posterization," where large areas become solid black or white, losing detail and shading.

**Dithering** solves this by arranging black and white pixels in patterns (similar to a chessboard) to simulate shades of gray.

- **Automatic Processing**: Images sent from the HMI Platform to the device are automatically dithered, requiring no user action.
- **Manual Tool**: We provide this standalone tool for developers. If you are developing for **Arduino** or **ESPHome** and want to display high-quality images on an E-ink screen, you can upload your image here, process it, and use the dithered result in your code.

## Tech Support & Product Discussion

Thank you for choosing our products! We are here to provide you with different support to ensure that your experience with our products is as smooth as possible. We offer several communication channels to cater to different preferences and needs.

<div class="table-center">
  <div class="button_tech_support_container">
  <a href="https://forum.seeedstudio.com/" class="button_forum"></a> 
  <a href="https://www.seeedstudio.com/contacts" class="button_email"></a>
  </div>

  <div class="button_tech_support_container">
  <a href="https://discord.gg/eWkprNDMU7" class="button_discord"></a> 
  <a href="https://github.com/Seeed-Studio/wiki-documents/discussions/69" class="button_discussion"></a>
  </div>
</div>











<!-- ---
title: Getting Started
description: How to register and login to SenseCraft HMI platform
---

Welcome to SenseCraft HMI! This guide will help you create an account and access the platform to start building beautiful e-paper display interfaces.

## Prerequisites

Before you begin, make sure you have:

- **Internet Connection**: Stable internet connection
- **Web Browser**: Modern browser (Chrome, Firefox, Safari, or Edge)
- **Email Address**: Valid email for account registration

## Step 1: Create Your Account

### Sign Up

1. Visit the [SenseCraft HMI platform](https://sensecraft-hmi.seeed.cc)
2. Click **"Log in"** in the top-right corner

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/canvas_51.png" style={{width:400, height:'auto'}}/></div>

3. If you don't already have a SenseCAP or SenseCraft account, please click “Sign up” at the bottom of the new page to register for one.

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/start_1.png" style={{width:400, height:'auto'}}/></div>

## Step 2: Login to the Platform

### Access Your Account

1. Go to the [SenseCraft HMI platform](https://sensecraft-hmi.seeed.cc)
2. Click **"Sign In"** in the top-right corner
3. Enter your email address and password
4. Check the box to agree to the privacy policy
5. Click **"Sign In"**

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/start_2.png" style={{width:400, height:'auto'}}/></div>

### Workspace Overview

<div style={{textAlign:'center'}}><img src="https://files.seeedstudio.com/wiki/reterminal_e10xx/sensecraft_hmi/start_3.png" style={{width:400, height:'auto'}}/></div>

Once logged in, you'll see the Workspace interface with:

- **Navigation Tabs**: Home, Workspace, and Tools tabs at the top
- **Device Section**: Shows your connected e-paper display devices
- **Device Card**: Displays device information including:
  - Device name (e.g., "e1001")
  - Device type (e.g., "reTerminal E1001")
  - MAC address
  - Device status (Online/Offline)
  - Battery level
  - Firmware version
- **Device Actions**: 
  - **Device Flasher**: Update device firmware
  - **+ Add Device**: Connect new e-paper displays

## Troubleshooting

### Common Login Issues

**Forgot Password**
- Click **"Forgot Password"** on the login page
- Enter your email address
- Check your email for password reset instructions

**Account Not Verified**
- Check your email inbox (including spam folder)
- Click the verification link in the email
- If the link expired, request a new verification email

**Login Problems**
- Ensure you're using the correct email address
- Check that Caps Lock is not enabled
- Clear your browser cache and cookies
- Try using a different browser

### Getting Help

- **Documentation**: Browse our comprehensive guides
- **[Community Forum](https://forum.seeedstudio.com/)**: Connect with other users
- **Support**: Contact our technical support team (techsupport@seeed.io)

---

**Congratulations!** You've successfully created your SenseCraft HMI account and can now access the platform.

*Ready to start building? Next, update your device firmware and then check out our other guides for device setup and project creation.* -->

