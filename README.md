# Hyprland Dotfiles

Personal dotfiles for a Debian-based Wayland setup.

## Features

- Hyprland
- Waybar
- Kitty
- Wofi
- Swaync
- Neofetch

- Custom Scripts:
  - `areascreenshot`: Area screenshot to clipboard
  - `startup.sh`: Launches Kitty and sets wallpaper
  - `change-theme.sh`: Cycles wallpapers and sends notifications
  - `waybar-tailscale.sh`: Tailscale VPN toggle and status for Waybar

---

## Directory Structure

```bash
~/.dotfiles
├── hypr/
│   └── .config/hypr/
│       ├── hyprland.conf
│       └── scripts/
│           ├── areascreenshot
│           └── startup.sh
├── kitty/
│   └── .config/kitty/
│       ├── kitty.conf
│       └── kitty-themes/
├── neofetch/
│   └── .config/neofetch/
│       └── config.conf
├── swaync/
│   └── .config/swaync/
│       ├── config.json
│       └── style.css
├── waybar/
│   └── .config/waybar/
│       ├── config
│       ├── config-with-power-menu
│       ├── style.css
│       ├── scripts/
│       │   ├── change-theme.sh
│       │   └── waybar-tailscale/using Hyprland, Waybar, Kitty, Wofi, Swaync, and more.

---
│       ├── config
│       ├── style.css
│       └── power-menu/
│           └── wofi-power-menu
└── README.md
```
Requirements

Tested on Debian stable.
Core packages

    hyprland

    waybar

    kitty

    wofi

    neofetch

    grim, slurp, wl-clipboard

    stow

Optional

    swww: Wallpaper daemon
    https://github.com/LGFae/swww

    swaync: Notification daemon
    https://github.com/ErikReider/SwayNotificationCenter

    tailscale: VPN and mesh networking
    https://tailscale.com

Installation

# Clone the repository
git clone https://github.com/yourusername/hyprland-dotfiles.git ~/.dotfiles
cd ~/.dotfiles

# Install required packages
sudo apt install stow hyprland waybar kitty wofi neofetch grim slurp wl-clipboard jq

# Stow configurations
stow hypr
stow kitty
stow neofetch
stow swaync
stow waybar
stow wofi

# Screenshots

Oran McClintock
oranmcclintock.com
github.com/sweeny68
