# PassWall2 OpenWrt Guide

# PassWall2 Installation Guide for OpenWrt 25.x

A practical installation and troubleshooting guide for running PassWall2 on modern OpenWrt releases.

This repository was created because many users experience dependency issues, package conflicts, or compatibility problems when installing PassWall2 on recent OpenWrt versions.

The guide is based on a real-world working setup and is intended to help users successfully deploy PassWall2 on newer OpenWrt systems.

---

## Tested Environment

| Component | Version |
|------------|------------|
| Device | Google WiFi (Gale) |
| Architecture | ARMv7 Processor rev 5 (v7l) |
| Target Platform | ipq40xx/chromium |
| OpenWrt | 25.12.4 r32933-4ccb782af7 |
| LuCI | openwrt-25.12 branch 26.158.67103~e99e132 |
| Kernel | 6.12.87 |
| PassWall2 | 26.6.3 |
| Xray | 26.6.27 |
| Sing-Box | 1.13.14 |
| Hysteria | 2.9.3 |
| Geoview | 0.2.6 |

---

## Purpose

This project aims to provide:

- A tested PassWall2 installation method
- OpenWrt 25.x compatibility notes
- Dependency troubleshooting
- Xray deployment guidance
- Google WiFi (Gale) specific recommendations

---

## Architecture Detection

The installation method used in this guide automatically detects the router architecture and downloads the correct package versions.

No manual architecture selection was required during installation.

Verified on:

- Google WiFi (Gale)
- ARMv7
- OpenWrt 25.12.4

---

## Storage Optimization

Many older routers have limited internal flash storage.

For this setup, Xray was successfully deployed using:

```text
/tmp/xray
```

instead of:

```text
/usr/bin/xray
```

Current working paths:

```text
Xray App Path:
/tmp/xray

Sing-Box App Path:
/usr/bin/sing-box

Hysteria App Path:
/usr/bin/hysteria

Geoview App Path:
/usr/bin/geoview
```

This approach helps reduce pressure on internal storage.

---

## Installation Overview

### Step 1

Update package lists.

### Step 2

Install required dependencies.

### Step 3

Install PassWall2.

### Step 4

Install Xray core.

### Step 5

Configure PassWall2.

### Step 6

Verify operation.

Detailed commands will be added in future updates.

---

## Troubleshooting

### Package Not Found

Verify package feeds are updated.

### Dependency Errors

Ensure all required repositories are available and compatible with your OpenWrt version.

### Xray Not Detected

Verify:

```text
/tmp/xray
```

exists and has executable permissions.

### Service Does Not Start

Check:

```bash
logread
```

and

```bash
dmesg
```

for detailed error messages.

---

## Screenshots

Screenshots will be added in future releases.

---

## Credits

PassWall2 is developed and maintained by its original developers.

This repository does not modify PassWall2 and only provides installation notes, troubleshooting information, and deployment guidance for OpenWrt users.

---

## Disclaimer

This guide is provided for educational and troubleshooting purposes.

Always create backups before modifying your router configuration.

Use at your own risk.

---

## Author

Johnny

Google WiFi (Gale) • OpenWrt 25.x • PassWall2
