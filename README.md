# Hyprland Dotfiles by Oran McClintock

Minimal, fast, and functional Wayland desktop powered by Hyprland. This setup is highly optimized for low resource usage and fast startup - ideal for daily productivity and older hardware.

> 🧠 **Idle RAM:** ~400–450MB  
> ⚡ **Boot time:** <10 seconds on Debian 13

  <img src="https://github.com/user-attachments/assets/ff01c611-0e0d-4d02-88ea-64ece6f6e592" >
  <img src="https://github.com/user-attachments/assets/ebdaadcc-2fc2-4d33-a2f7-7b9fdd57c8a6" >


---

## 📁 Structure

```bash
~/.Hyprland-dotfiles
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
│       │   └── waybar-tailscale
│       │
│       ├── config
│       ├── style.css
│       └── power-menu/
│           └── wofi-power-menu
└── README.md
```

---

## 🛠 Features

- Dual-monitor layout (eDP-1 + HDMI-A-1)  
- Rounded corners, blur, shadows, gaps  
- Fast startup wallpaper + neofetch  
- Toggle scripts for Waybar and Bluetooth  
- Area screenshot tool with clipboard + notification  
- Media keys for volume, brightness, and player control  
- Lightweight terminal with themed Kitty setup  

---

## 🔧 Scripts

Located in `~/.config/hypr/scripts/`:

| Script               | Description                        |
|----------------------|----------------------------------|
| `startup.sh`         | Sets wallpaper and runs neofetch |
| `areascreenshot`     | Grim + slurp screenshot tool     |
| `start-bluetooth.sh` | Starts Bluetooth daemon + applet |
| `toggle_waybar.sh`   | Toggles Waybar and SwayNC        |

---

## ⚙ Requirements

Install the following packages:

```bash
sudo apt install hyprland kitty waybar wofi swaync \
blueman grim slurp wl-clipboard swww \
brightnessctl pamixer playerctl neofetch
```

## 🚀 Installation

```bash
git clone https://github.com/sweeny68/hyprland-dotfiles.git
cd hyprland-dotfiles
```

# Backup existing configs if needed
```bash
mkdir -p ~/.config_backup
mv ~/.config/hypr ~/.config_backup/
```

# Copy configs
```bash
cp -r hypr/.config/hypr ~/.config/
cp -r kitty/.config/kitty ~/.config/
cp -r swaync/.config/swaync ~/.config/
cp -r waybar/.config/waybar ~/.config/
cp -r wofi/.config/wofi ~/.config/
cp -r neofetch/.config/neofetch ~/.config/
```
# Make scripts executable

```bash
chmod +x ~/.config/hypr/scripts/*.sh
```

## Keybindings 

| Keybinding            | Action                   |
|-----------------------|--------------------------|
| `SUPER + Return`      | Open Kitty terminal      |
| `SUPER + Space`       | Launch Wofi              |
| `SUPER + Tab`         | Toggle Waybar / SwayNC   |
| `CTRL + SHIFT + 4`    | Area screenshot          |
| `XF86Audio*`          | Media controls (audio)   |
| `XF86MonBrightness*`  | Media controls (brightness) |

- Oran McClintock
- oranmcclintock.com

