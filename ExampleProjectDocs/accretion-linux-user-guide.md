# Accretion Linux User Guide

## Table of Contents

1. Introduction
2. System Requirements
3. Installation
4. Getting Started
5. Desktop Environment
6. System Configuration
7. Software Management
8. Networking
9. Troubleshooting
10. Support and Community

## 1. Introduction

Welcome to Accretion Linux! This guide will help you get started with your new operating system and provide information on its key features and usage.

## 2. System Requirements

- CPU: 64-bit x86 processor (x86_64)
- RAM: Minimum 2GB, 4GB recommended
- Storage: At least 20GB of free space
- Graphics: Any modern graphics card with 3D acceleration
- Internet connection for updates and additional software

## 3. Installation

1. Download the Accretion Linux ISO from our official website.
2. Create a bootable USB drive using tools like Etcher or Rufus.
3. Boot your computer from the USB drive.
4. Follow the on-screen instructions in our graphical installer.
5. Choose your language, timezone, and keyboard layout.
6. Partition your disk as needed (the installer offers guided options).
7. Create your user account and password.
8. Wait for the installation to complete and reboot.

## 4. Getting Started

After installation, you'll be greeted by the login screen. Enter your username and password to access your desktop.

## 5. Desktop Environment

Accretion Linux uses a customized version of XFCE as its default desktop environment.

- The top panel contains the application menu, quick launch icons, and system tray.
- The desktop allows you to organize files and create shortcuts.
- Right-click on the desktop or panel for customization options.

## 6. System Configuration

- System Settings: Access from the application menu or by right-clicking the desktop.
- Key areas include:
  - Appearance: Customize themes, icons, and fonts
  - Display: Adjust resolution and multi-monitor setup
  - Power Management: Configure energy saving options
  - User Accounts: Manage users and groups

## 7. Software Management

Accretion Linux uses a custom package manager called AccretionPM.

- Open the Software Center from the application menu to browse and install software.
- Use the terminal for advanced package management:
  - Install a package: `sudo apm install package_name`
  - Remove a package: `sudo apm remove package_name`
  - Update the system: `sudo apm update && sudo apm upgrade`

## 8. Networking

- Click the network icon in the system tray to manage connections.
- For Wi-Fi, select your network and enter the password when prompted.
- For advanced network configuration, use the Network Manager tool in System Settings.

## 9. Troubleshooting

- If you encounter issues, check our FAQ at https://accretionlinux.org/faq
- For graphics issues, try booting in safe mode by selecting it from the boot menu.
- For package conflicts, use `sudo apm check` to verify system integrity.

## 10. Support and Community

- Official forums: https://forums.accretionlinux.org
- IRC channel: #accretion on irc.freenode.net
- Bug reports: https://gitea.accretionlinux.org/accretion/issues
- Wiki: https://wiki.accretionlinux.org

Thank you for choosing Accretion Linux. We hope you enjoy using our distribution!
