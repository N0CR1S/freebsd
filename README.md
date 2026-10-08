# My Suckless Desktop

My personal configuration for a minimal Linux desktop built around
[Suckless](https://suckless.org/) software.

The setup currently contains:

- **dwm** — dynamic window manager
- **st** — simple terminal
- **dmenu** — application launcher
- **slstatus** — status bar

The configuration focuses on simplicity, minimalism, and a consistent dark
color scheme.

---

## Preview

The setup uses a dark gray background with muted gray text and red accents.

### Color palette

| Name | Color |
|------|-------|
| Background | `#161b22` |
| Dark gray | `#2a313b` |
| Foreground | `#aab0bb` |
| Bright foreground | `#eceff4` |
| Accent | `#c25555` |

The same palette is used throughout the desktop configuration.

---

## Components

### dwm

The window manager is configured with:

- 9 tags/workspaces
- Tiling, floating, and monocle layouts
- A `0.55` master-area factor
- 1 master client by default
- 120 Hz refresh rate
- Super/Windows key as the main modifier
- `st` as the default terminal
- `dmenu_run` as the application launcher

The default layouts are:

```text
[]=
><>
[M]
```

The first layout is the default tiled layout.

---

### dmenu

dmenu is configured with:

- Top-bar placement
- `monospace:size=10`
- Dark background
- Light gray text
- Red selection color

The colors are:

```text
Normal:
  foreground: #aab0bb
  background: #161b22

Selected:
  foreground: #eceff4
  background: #c25555
```

---

### slstatus

slstatus provides the information displayed in the status bar.

The current configuration includes support for displaying:

- Date and time
- Battery percentage
- Battery remaining time
- Battery charging state
- CPU frequency
- CPU usage
- Disk usage
- Disk space
- RAM usage
- Swap usage
- Network speed
- Wi-Fi information
- IP addresses
- Hostname
- Kernel version
- Uptime
- Temperature
- Volume
- Username
- Custom shell commands

The current status configuration displays the date and time using:

```text
%F %T
```

with a one-second update interval.

---

## Keybindings

The main modifier is:

```text
Super / Windows key
```

### Applications

| Key | Action |
|-----|--------|
| `Super + P` | Launch dmenu |
| `Super + Shift + Enter` | Launch terminal |
| `Super + B` | Toggle status bar |

### Window management

| Key | Action |
|-----|--------|
| `Super + J` | Focus next window |
| `Super + K` | Focus previous window |
| `Super + Shift + C` | Close focused window |
| `Super + Space` | Toggle layout |
| `Super + Shift + Space` | Toggle floating |
| `Super + Enter` | Zoom/promote window |

### Master area

| Key | Action |
|-----|--------|
| `Super + I` | Increase number of master windows |
| `Super + D` | Decrease number of master windows |
| `Super + H` | Decrease master area size |
| `Super + L` | Increase master area size |

### Layouts

| Key | Layout |
|-----|--------|
| `Super + T` | Tiling |
| `Super + F` | Floating |
| `Super + M` | Monocle |

### Tags

| Key | Action |
|-----|--------|
| `Super + 1` ... `Super + 9` | View tag |
| `Super + Shift + 1` ... `9` | Move window to tag |
| `Super + 0` | View all tags |
| `Super + Shift + 0` | Tag window with all tags |

### Monitors

| Key | Action |
|-----|--------|
| `Super + ,` | Focus previous monitor |
| `Super + .` | Focus next monitor |
| `Super + Shift + ,` | Move window to previous monitor |
| `Super + Shift + .` | Move window to next monitor |

### Quit

```text
Super + Shift + Q
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

The Suckless programs are configured by editing their respective
`config.h` files and compiling them.

### dwm

```bash
cd dwm
sudo make clean install
```

### dmenu

```bash
cd dmenu
sudo make clean install
```

### slstatus

```bash
cd slstatus
sudo make clean install
```

### st

```bash
cd st
sudo make clean install
```

> Replace the commands above with your preferred build/install method if you
> don't want to install system-wide.

---

## Configuration Structure

A typical repository layout is:

```text
.
├── dwm/
│   └── config.h
│
├── dmenu/
│   └── config.h
│
├── slstatus/
│   └── config.h
│
├── st/
│   └── config.h
│
└── README.md
```

---

## Philosophy

This configuration follows the general Suckless philosophy:

- Keep the desktop simple
- Avoid unnecessary graphical software
- Configure software through source code
- Prefer keyboard-driven workflows
- Keep dependencies minimal
- Use a consistent visual theme

The goal is a desktop that stays out of the way and lets the applications
do the work.

---

## Theme

The main accent color is:

```text
#c25555
```

The primary background is:

```text
#161b22
```

and the main foreground is:

```text
#aab0bb
```

This gives the desktop a dark, low-contrast appearance with a muted red
accent.

---

## Credits

This configuration is built around software from the
[Suckless](https://suckless.org/) project.

- [dwm](https://dwm.suckless.org/)
- [dmenu](https://tools.suckless.org/dmenu/)
- [st](https://st.suckless.org/)
- [slstatus](https://tools.suckless.org/slstatus/)

Configuration files in this repository are personal modifications of the
respective Suckless configuration files.

See the individual projects and their `LICENSE` files for licensing
information.

---

## Disclaimer

This is a personal configuration.

You may need to modify paths, fonts, keyboard layouts, monitor settings,
and commands depending on your system.
