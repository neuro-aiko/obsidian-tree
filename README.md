# Android device tree for Android mainline (generic)

```
#
# SPDX-FileCopyrightText: The LineageOS Project
# SPDX-License-Identifier: Apache-2.0
#
```
# Obsidian — HyperOS 3 Project Tree

> Organized project tree for the **Obsidian** device running **HyperOS 3 based on Android 16**.

## Overview

This repository provides an organized structure for the **Obsidian** device, including the components required for Android development and firmware work.

The goal is to keep device-specific files separated into clear and maintainable directories.

## Device Information

| Property         | Value      |
| ---------------- | ---------- |
| Device codename  | `Obsidian` |
| Operating system | HyperOS 3  |
| Android version  | Android 16 |
| Architecture     | ARM64      |

## Directory Structure

```text
.
├── BoardConfig.mk
├── AndroidProducts.mk
├── Android.bp
├── Android.mk
├── device.mk
├── vendorsetup.sh
│
├── configs/
│   └── Device-specific configuration files
│
├── overlay/
│   └── Android resource overlays
│
├── proprietary/
│   └── Device-specific proprietary files
│
├── rootdir/
│   └── Device-specific root filesystem configuration
│
├── sepolicy/
│   └── SELinux policies
│
├── init/
│   └── Device-specific init scripts
│
├── kernel/
│   └── Kernel configuration and related files
│
└── README.md
```

## Main Components

### `BoardConfig.mk`

Contains the board-level configuration used by the Android build system.

### `device.mk`

Defines device-specific packages, properties and configuration included in the build.

### `AndroidProducts.mk`

Registers the available Android product definitions for the device.

### `Android.bp` / `Android.mk`

Contains build definitions for device-specific components.

### `vendorsetup.sh`

Provides the device lunch/build configuration to the Android build environment.

### `overlay/`

Contains resource overlays used to customize Android behavior and resources for the device.

### `proprietary/`

Contains proprietary device-specific components required by the hardware and software stack.

### `rootdir/`

Contains device-specific files used during early Android boot.

### `init/`

Contains device-specific initialization scripts and services.

### `sepolicy/`

Contains SELinux policy definitions required by the device.

### `kernel/`

Contains kernel-related configuration and source components when included in the project.

## Organization

The tree follows the standard Android device-tree structure where possible, while keeping device-specific components isolated from the Android platform source.

This makes the project easier to:

* Maintain
* Port between Android versions
* Integrate into custom ROM projects
* Debug device-specific issues
* Review changes
* Build reproducibly

## Status

This project is under active development.

Some components may still require additional configuration or adaptation for a complete Android build.
