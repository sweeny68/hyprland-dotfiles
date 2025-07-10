# 🌀 Hyprland Dotfiles by Oran McClintock

Minimal, fast, and functional Wayland desktop powered by Hyprland. This setup is highly optimized for low resource usage and fast startup — ideal for daily productivity and older hardware.

> 🧠 **Idle RAM:** ~400–450MB  
> ⚡ **Boot time:** <10 seconds on Debian 12

---

## 📁 Structure

~/.config/
├── hypr/ # Hyprland config + launch scripts
├── kitty/ # Kitty terminal + 100+ themes
├── swaync/ # Notifications (SwayNC)
├── waybar/ # Status bar (custom modules)
├── wofi/ # Launcher + power menu
├── neofetch/ # System info


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

| Script               | Description                         |
|----------------------|-------------------------------------|
| `startup.sh`         | Sets wallpaper and runs neofetch   |
| `areascreenshot`     | Grim + slurp screenshot tool       |
| `start-bluetooth.sh` | Starts Bluetooth daemon + applet   |
| `toggle_waybar.sh`   | Toggles Waybar and SwayNC          |

---

## ⚙ Requirements

Install the following packages:

```bash
sudo apt install hyprland kitty waybar wofi swaync \
blueman grim slurp wl-clipboard swww \
brightnessctl pamixer playerctl neofetch

---

## 🚀 Installation

git clone https://github.com/sweeny68/hyprland-dotfiles.git
cd hyprland-dotfiles

# Backup existing configs if needed
mkdir -p ~/.config_backup
mv ~/.config/hypr ~/.config_backup/hypr_$(date +%s) 2>/dev/null

# Copy configs
cp -r hypr/.config/hypr ~/.config/
cp -r kitty/.config/kitty ~/.config/
cp -r swaync/.config/swaync ~/.config/
cp -r waybar/.config/waybar ~/.config/
cp -r wofi/.config/wofi ~/.config/
cp -r neofetch/.config/neofetch ~/.config/

# Make scripts executable
chmod +x ~/.config/hypr/scripts/*.sh

🎮 Keybindings (Hyprland)
Keybind	Action
SUPER + Return	Open Kitty terminal
SUPER + Space	Launch Wofi
SUPER + Tab	Toggle Waybar/SwayNC
CTRL + SHIFT + 4	Area screenshot
XF86Audio* / XF86MonBrightness*	Media controls
👤 Author

Oran McClintock
oranmcclintock.com
@sweeny68
📄 License

MIT

---