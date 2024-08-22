# Acreetion Linux: Minimum Viable Product (MVP) Specification

## 1. Introduction

This document outlines the Minimum Viable Product (MVP) for Acreetion Linux, a custom Linux distribution aimed at providing a lightweight and versatile operating system. The MVP represents the core features and functionality that must be implemented for the ***initial release.***

## 2. MVP Goals

1. Create a bootable Linux distribution
2. Provide basic system functionality
   1. Boot into options
      1. Startx/Cinnamon
      2. Start AcreetionOSInstaller
      3. Start the Archinstall Script
3. Include essential software for daily use
4. Ensure stability and performance on target hardware
5. Implement a simple update mechanism

## 3. Core Features

### 3.1 System Base
- Linux Kernel (latest Zen version)
  1. Latest Zen Kernel version compiled by Bot.
- Systemd init system
- Basic system utilities (coreutils, util-linux, etc.) GNU-Utils, Parted, Fdisk, Gnome-disk-utility...
[PackageList]() - [ ] ToDo Link to package list

### 3.2 User Interface
- Desktop Environment (Cinnamon)
- Display manager (LightDM)
- Basic theme and icon set

### 3.3 Package Management
- flatpak, pacman, AUR (Unofficially)

### 3.4 Pre-installed Software
- Web browser (Firefox)
- Text-editor 
- Gnome-Console
- Nemo
- Gnome-System-Monitor
- Pamac
- touchegg
- xf86-video-amdgpu
- xf86-video-ati
- xf86-video-intel
- xf86-video-qxl
- xf86-input-vmmouse
- xf86-video-vmware
- virtualbox-guest-utils

### 3.5 Hardware Support
- Generic drivers for common hardware components
- Automated hardware detection
- Basic power management
- - [ ] NVidia Support? 
- - [ ] ARC Support?
- - 
### 3.6 Networking
- Network Manager for Wi-Fi and Ethernet connections
- Basic firewall configuration
- - NetworkManager (NMCLI)
- 
### 3.7 System Installation
- Live system environment
- CLI installer with basic options:
  - Disk partitioning
  - User account creation
  - Language/locale selection
  - Set timezone
  - Use Pacstrap to install basic system packages
  - Generate FSTAB using genfstab
  - Write hostname
  - Generate Initramfs using mkinitcpio
  - Disabling Root Account
  - Install other packages using pacman after CHROOT
  - Bootloader Installation

### 3.8 Update System
- Basic system update mechanism through pacman/pamac.

## 4. Non-Features (Postponed for Future Releases)
- Not giving a custom theme 
- Not Giving a antivirus
- No full disk encryption
- No Advanced power management
- NO WINE
- No Advanced development tools
- No support for other Desktop Environments Officially.
- Not Supporting the AUR
- Not Supporting Flatpak packages themselves
- Not Supporting/Installing Snapd.

## 5. Performance Targets

- Boot time: Under 30 seconds on target hardware
- RAM usage at idle: Less than 4G
- Disk space for base system: Under 20GB

## 6. Target Hardware

- CPU: 64-bit x86 processors (x86_64)
- RAM: Minimum 8GB
- Storage: Minimum 128GB
- Graphics: Basic GPU with 3D acceleration

## 7. Success Criteria

The MVP will be considered successful if:

1. The system successfully installs on target hardware
2. All core features function as described
3. The system remains stable under normal use conditions
4. Performance targets are met
5. Basic daily computing tasks can be accomplished

## 8. Future Considerations

While out of scope for the MVP, the following areas will be prioritized for future development:

1. Expanded software repository
2. Advanced system configuration tools
3. Improved hardware support
4. Enhanced security features
5. Developer-focused tools and environments

This MVP specification provides a clear, focused target for our initial release of Accretion Linux. It ensures we deliver a functional, albeit basic, operating system that can serve as a foundation for future enhancements.

