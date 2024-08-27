# AcreetionOS Linux: Architecture Overview

## 1. Introduction
[Summerize when the rest of the document is finished]

## 2. System Architecture

AcreetionOS Linux follows a modular architecture, built on top of the Linux kernel. The system is composed of the following major components:

### User Applications
|Self-Created| Community Created|
| ---------- | ---------------- |
| CInstaller |Archinstall     |
|            |Mate Terminal |
|            |gedit|
|            |VS Code |
|            |Nano|
|            |VI|
|            |xviewer
|            |xreader
|            |xarchiver
|            |xplayer
|            |pix 

### Desktop Environment
***Cinnamon***, *Mate, XFCE*

### System Services 
*Lightdm*
*timeshift*
*Pamac update start up service thing*

### Package Manager
*Pacman, AUR, Flatpak* 

### Init System
*Systemd*

### Linux Kernel
*Zen-Kernel*

### Hardware
*x86_64*


### 2.1 Linux Kernel

At the core of AcreetionOS Linux, we are using the Zen Kernel, a kernel with a variety of extra patches for performance improvements. It is managed by The Zen Kernel team found at https://github.com/zen-kernel/zen-kernel. 

### 2.2 Init System

Acreetion Linux uses systemd as its init system and service manager, handling the boot process and managing system services.

### 2.3 System Services

These include essential daemons and background processes such as:
- NetworkManager for network configuration
- Pipewire for audio management
- Xorg for display server

### 2.5 Desktop Environment

## 3. Key Subsystems

### 3.1 Boot Process

1. Systemd-boot
2. Linux kernel initialization
5. Display manager launch
6. User session start

### 3.2 File System Hierarchy

Follows the Filesystem Hierarchy Standard (FHS) with some custom directories:
- /etc/accretion for system-wide configuration
- /usr/lib/accretion for Accretion-specific libraries
- /opt/accretion for optional Accretion-specific software

### 3.3 User Management

Utilizes systemd-logind for user session management and PAM for authentication.

### 3.4 Networking

NetworkManager handles network connections, with a custom GUI front-end for easy user configuration.

## 4. Security Architecture

- SELinux for mandatory access control
- AppArmor profiles for application sandboxing
- Regular security updates through the package manager
- Firewall management through ufw (Uncomplicated Firewall)

## 5. Customization and Extension

- A plugin system for the desktop environment allows easy customization
- A well-defined API for system utilities to interact with core components
- Hook scripts in the package manager for custom actions during package operations

## 6. Build and Release Process

- Automated build system using Jenkins
- ISO creation using custom scripts based on archiso
- Continuous Integration/Continuous Deployment (CI/CD) pipeline for testing and releasing

This architecture is designed to be modular and flexible, allowing for easy customization and extension as the project evolves.

