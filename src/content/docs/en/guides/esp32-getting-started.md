---
title: ESP32-S3 E-Paper Display Setup Guide | Seeed Studio
description: Complete guide to setting up ESP32-S3 with e-paper displays using SenseCraft HMI. Build your first no-code dashboard in minutes.
sidebar:
  order: 1
---

# Getting Started with ESP32-S3 E-Paper Displays

Build your first e-paper interface using **Seeed Studio's reTerminal E series** and the **ESP32-S3** microcontroller. This guide covers everything from hardware setup to creating your first no-code dashboard.

## Why Choose ESP32-S3 for E-Paper?

The **ESP32-S3** is the perfect match for e-paper displays:
- **Ultra-low power consumption** - 3-month battery life
- **Wi-Fi & Bluetooth** built-in
- **8MB PSRAM** for complex UIs
- **Hardware acceleration** for graphics

## Hardware Requirements

### Seeed reTerminal E Series
- **E1001**: 7.5" monochrome e-paper display
- **E1002**: 7.3" full-color E Ink Spectra 6 display

### Key Features
- **Processor**: ESP32-S3 dual-core 240MHz
- **Memory**: 8MB Flash, 8MB PSRAM
- **Connectivity**: Wi-Fi 802.11 b/g/n, Bluetooth 5.0
- **Sensors**: Temperature & humidity built-in
- **Power**: 3.7V battery support with charging

## Quick Start

### Step 1: Connect Your Display
```bash
# Connect via USB-C to your computer
# The device will appear as a serial port
```

### Step 2: Open SenseCraft HMI
Visit the web-based designer - no installation required!

### Step 3: Design Your Interface
- Drag and drop widgets
- Configure data sources
- Preview in real-time

### Step 4: Deploy to ESP32-S3
One-click deployment to your device.

## Home Assistant Integration

Connect your ESP32 e-paper display to Home Assistant:

```yaml
# configuration.yaml
mqtt:
  sensor:
    - name: "E-Paper Temperature"
      state_topic: "sensecraft/epaper/temperature"
      unit_of_measurement: "°C"
```

## TRMNL Alternative Features

Looking for an open-source TRMNL alternative? SenseCraft HMI offers:
- **No subscription fees**
- **Local control** - no cloud required
- **Open-source** community
- **Customizable** widgets

## Example Projects

### Weather Dashboard
Display real-time weather on your e-paper screen using ESP32-S3's Wi-Fi capabilities.

### Smart Home Controller
Control lights, temperature, and security from a beautiful e-ink interface.

### Information Display
Perfect for office spaces, showing calendars, tasks, and notifications.

## Power Optimization Tips

Maximize your ESP32-S3 battery life:
1. Use deep sleep between updates
2. Optimize refresh intervals
3. Leverage partial refresh for e-paper
4. Disable Wi-Fi when not needed

## Next Steps

- [Home Assistant Integration Guide](/en/guides/home-assistant)
- [Advanced ESP32 Programming](/en/guides/esp32-programming)
- [Battery Optimization](/en/guides/power-management)

---

*Building with Seeed Studio's ESP32-S3 e-paper displays? Share your projects in our [community forum](https://forum.seeedstudio.com)!*