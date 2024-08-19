# Accretion Linux Developer Guide

## Table of Contents

1. Introduction
2. Setting Up the Development Environment
3. Project Structure
4. Building Accretion Linux
5. Package Management
6. Contributing to Accretion Linux
7. API Reference
8. Testing
9. Continuous Integration/Continuous Deployment (CI/CD)
10. Release Process

## 1. Introduction

Welcome to the Accretion Linux Developer Guide. This document provides information and guidelines for developers who want to contribute to Accretion Linux or build software for it.

## 2. Setting Up the Development Environment

### Requirements:
- A Linux-based OS (Accretion Linux or another distribution)
- Git
- GCC and related build tools
- Python 3.8+

### Setup Steps:
1. Clone the repository:
   ```
   git clone https://gitea.accretionlinux.org/accretion/accretion-linux.git
   ```
2. Install dependencies:
   ```
   cd accretion-linux
   ./scripts/install_deps.sh
   ```

## 3. Project Structure

```
accretion-linux/
├── src/
│   ├── kernel/
│   ├── bootloader/
│   ├── package-manager/
│   └── system-config/
├── packages/
├── scripts/
├── docs/
└── tests/
```

## 4. Building Accretion Linux

To build Accretion Linux:

1. Set up the build environment:
   ```
   ./scripts/setup_build_env.sh
   ```
2. Configure the build:
   ```
   ./configure --prefix=/usr --enable-optimizations
   ```
3. Build the system:
   ```
   make
   ```
4. Create an ISO:
   ```
   make iso
   ```

## 5. Package Management

Accretion Linux uses a custom package manager, AccretionPM. To create a new package:

1. Create a package definition file (`package.acr`) in the `packages/` directory.
2. Use the `apm-build` tool to create the package:
   ```
   apm-build packages/mypackage/package.acr
   ```

## 6. Contributing to Accretion Linux

1. Fork the repository on our Gitea server.
2. Create a new branch for your feature or bug fix.
3. Make your changes, following our coding style guidelines.
4. Write or update tests as necessary.
5. Submit a pull request with a clear description of your changes.

See CONTRIBUTING.md for more detailed information.

## 7. API Reference

Accretion Linux provides several APIs for system integration. See the API Documentation for detailed information. Key APIs include:

- AccretionPM API for package management
- System Configuration API
- Hardware Abstraction Layer (HAL) API

## 8. Testing

Run the test suite:
```
make test
```

Write new tests in the `tests/` directory, following the existing structure.

## 9. Continuous Integration/Continuous Deployment (CI/CD)

We use Jenkins for our CI/CD pipeline. On every pull request:

1. The system is built
2. All tests are run
3. A test ISO is created
4. The test ISO is booted in a virtual machine for integration testing

## 10. Release Process

1. Update the changelog
2. Tag the release in git
3. Build release candidates for testing
4. Once approved, build the final release
5. Update the website and release announcements

For more detailed information on any of these topics, please refer to our developer wiki at https://wiki.accretionlinux.org/dev

Happy coding, and thank you for contributing to Accretion Linux!
