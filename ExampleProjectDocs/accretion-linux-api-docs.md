# Accretion Linux API Documentation

## Introduction

This document outlines the key APIs provided by Accretion Linux for system integration and extension. These APIs allow developers to interact with core system components, create plugins, and build applications that integrate deeply with Accretion Linux.

## 1. Package Management API

### 1.1 AccretionPackageManager

The `AccretionPackageManager` class provides methods for interacting with the system's package management.

#### Methods:

```python
def install_package(package_name: str) -> bool:
    """Install a package by name."""

def remove_package(package_name: str) -> bool:
    """Remove a package by name."""

def update_system() -> bool:
    """Update all packages on the system."""

def query_package(package_name: str) -> dict:
    """Get information about a specific package."""
```

## 2. System Configuration API

### 2.1 AccretionConfig

The `AccretionConfig` class allows reading and modifying system-wide configuration settings.

#### Methods:

```python
def get_config(key: str) -> str:
    """Retrieve a configuration value."""

def set_config(key: str, value: str) -> bool:
    """Set a configuration value."""

def list_configs() -> List[str]:
    """List all available configuration keys."""
```

## 3. User Management API

### 3.1 AccretionUserManager

The `AccretionUserManager` class provides methods for managing user accounts.

#### Methods:

```python
def create_user(username: str, password: str) -> bool:
    """Create a new user account."""

def delete_user(username: str) -> bool:
    """Delete a user account."""

def modify_user(username: str, **kwargs) -> bool:
    """Modify user account properties."""
```

## 4. Hardware Information API

### 4.1 AccretionHardwareInfo

The `AccretionHardwareInfo` class provides methods for querying system hardware information.

#### Methods:

```python
def get_cpu_info() -> dict:
    """Retrieve CPU information."""

def get_memory_info() -> dict:
    """Retrieve memory information."""

def get_disk_info() -> List[dict]:
    """Retrieve disk information."""
```

## 5. Networking API

### 5.1 AccretionNetworkManager

The `AccretionNetworkManager` class provides methods for managing network connections.

#### Methods:

```python
def list_connections() -> List[dict]:
    """List all network connections."""

def connect(connection_id: str) -> bool:
    """Connect to a network."""

def disconnect(connection_id: str) -> bool:
    """Disconnect from a network."""
```

## 6. Desktop Environment API

### 6.1 AccretionDesktopManager

The `AccretionDesktopManager` class provides methods for interacting with the desktop environment.

#### Methods:

```python
def get_current_theme() -> str:
    """Get the current desktop theme."""

def set_theme(theme_name: str) -> bool:
    """Set the desktop theme."""

def list_installed_applications() -> List[str]:
    """List all installed desktop applications."""
```

## Usage Example

Here's a simple example of how to use the Package Management API:

```python
from accretion.package import AccretionPackageManager

# Create an instance of the package manager
pm = AccretionPackageManager()

# Install a package
if pm.install_package("firefox"):
    print("Firefox installed successfully")
else:
    print("Failed to install Firefox")

# Query package information
firefox_info = pm.query_package("firefox")
print(f"Installed Firefox version: {firefox_info['version']}")
```

## Error Handling

All API methods may raise `AccretionAPIError` exceptions. It's recommended to catch and handle these exceptions appropriately in your applications.

## Versioning

This API documentation is for Accretion Linux version 1.0. API compatibility is guaranteed for all 1.x versions.

