# NixOS-Config

A simple, atomic NixOS flake configuration with Hyprland window manager.

## Overview

This repository contains my personal NixOS configuration as a flake. It provides a reproducible, declarative setup for a desktop environment with Hyprland, SDDM, and a curated set of packages.

## Features

- **Hyprland** tiling window manager with custom themes
- **SDDM** display manager with Sugar Dark and Tokyo Night themes
- **Home Manager** integration for user environment
- **Atomic upgrades** — roll back to any previous generation
- **Live installer** — boot from ISO and install interactively

## Quick Start

### From a NixOS ISO

```bash
curl -L https://raw.githubusercontent.com/dev-spectre/NixOS-Config/main/install.sh | bash
```

### Manual

```bash
git clone https://github.com/dev-spectre/NixOS-Config.git
cd NixOS-Config
sudo nixos-rebuild switch --flake .#Default
```

## Project Structure

```
├── flake.nix              # Flake entry point
├── install.sh             # Entry installer (detects live env)
├── live-install.sh        # Interactive installer for live ISO
├── hosts/
│   └── Default/           # Host-specific configuration
│       ├── configuration.nix
│       ├── hardware-configuration.nix
│       ├── host-packages.nix
│       └── variables.nix
├── modules/               # Shared NixOS modules
├── pkgs/                  # Custom packages (SDDM themes, etc.)
└── LICENSE
```

## License

MIT
