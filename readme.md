# Intune Autopilot OOBE Deployment

## Overview

This repository documents the manual Intune Autopilot enrollment process performed during Windows OOBE (Out-of-Box Experience) using Shift + F10.

It allows an IT technician to:
- Capture device hardware identity
- Upload device to Microsoft Intune Autopilot
- Enable zero-touch provisioning

---

## Network Requirement

- Plug in Ethernet cable (device gets internet via DHCP)
- Internet is required for PowerShell downloads and Intune upload

---

## Process

Steps are documented here:

[Setup Process](Setup.md)

---

## Result

- Device is registered in Intune Autopilot
- Hardware hash is stored in Microsoft cloud
- Device will auto-enroll on next boot