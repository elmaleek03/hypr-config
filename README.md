# Hyprland Config (Personal)

My personal Hyprland configuration for CachyOS with [Omarchy](https://omarchy.org/).

These files live in `~/.config/hypr/` and override the default Omarchy settings sourced from `~/.local/share/omarchy/default/hypr/`.

## Changes from Default Omarchy

### Input & Gestures (`input.conf`)
- Natural scroll enabled on touchpad
- Clickfinger behavior (two-finger = right-click)
- Scroll factor reduced to `0.2` for finer control
- Keyboard repeat rate `40` / delay `250` (faster than default)
- Caps Lock mapped as actual Caps Lock (not Compose)
- **macOS-like workspace swipe gestures:**
  - `workspace_swipe_cancel_ratio = 0.15` (commits early, default is 0.5)
  - `workspace_swipe_min_speed_to_force = 10` (light flick triggers switch)
  - `workspace_swipe_distance = 300` (natural 1:1 tracking)
- 4-finger horizontal swipe for workspace switching
- 3-finger left/right for focus movement
- Per-app touchpad scroll tuning (Alacritty, Ghostty, VS Code)

### Look & Feel (`looknfeel.conf`)
- Shadows disabled (battery saving)
- **macOS-style workspace animation:** custom bezier `(0.16, 1.0, 0.3, 1.0)` with slower duration for smooth, gliding transitions

### Monitors (`monitors.conf`)
- Laptop: `eDP-1` at 2880x1800@120Hz, scale 1.6, VRR enabled
- External: MSI MD272QXP at 2560x1440@100Hz, scale 1.25 (DP-1/DP-2)
- `GDK_SCALE=2`, XWayland force zero scaling for crisp fractional scaling
- Qt auto screen scale enabled

### Keybindings (`bindings.conf`)
- Custom app launchers (Nautilus, Obsidian, Typora, Signal, 1Password, etc.)
- Web app shortcuts (ChatGPT, Grok, Hey Calendar/Email, YouTube, WhatsApp, X)
- Power profile cycling (`SUPER+CTRL+P`)

### Main Config (`hyprland.conf`)
- Sources Omarchy defaults then overrides with personal configs
- Hypr session saver enabled
- HyprEmoji integration

## Setup

```bash
# Clone and symlink
git clone <this-repo> ~/projects/hypr-config
ln -sf ~/projects/hypr-config ~/.config/hypr
```

Or copy individual files into `~/.config/hypr/`.

## System

- **OS:** CachyOS (Arch-based)
- **WM:** Hyprland 0.54.3
- **Desktop:** Omarchy
- **Laptop:** 2880x1800 120Hz display
