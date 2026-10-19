# Waybar Configuration

[![GitHub repository](https://img.shields.io/badge/GitHub-xodo2fast4u%2Fwaybar-181717?logo=github&style=for-the-badge)](https://github.com/xodo2fast4u/waybar)
[![License: MIT](https://img.shields.io/badge/license-MIT-2E8B57?style=for-the-badge)](./LICENSE)

A personal, dark-themed [Waybar](https://github.com/Alexays/Waybar) setup for a
Hyprland desktop. The bar places workspace and window information on the left,
a clock in the center, and system controls and status indicators on the right.

## What's included

- **Hyprland workspaces:** Displays workspaces 1–5 on every output, sorted by
  number, with application icons and window taskbar indicators.
- **Active window:** Shows the current window title, truncated to 30 characters.
- **Clock:** Displays the time in `Africa/Johannesburg`; its alternate view shows
  the date, and its tooltip contains a calendar.
- **System status:** Shows idle-inhibitor state, network connection and traffic,
  audio volume, CPU usage, memory usage, and the system tray.
- **Dark styling:** Rounded modules, subtle gradients, and JetBrainsMono Nerd
  Font typography.

## Requirements

- [Waybar](https://github.com/Alexays/Waybar) with Hyprland module support
- [Hyprland](https://hyprland.org/)
- [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads) for the
  configured font and icon glyphs
- [Papirus-Dark](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme)
  icon theme for workspace application icons
- `kitty` and `btop` for the CPU and memory click actions
- `pavucontrol` for the audio click action

The configuration refers to these programs by name. Install them using your
distribution's package manager, or adjust the commands and icon theme in
`config.jsonc` to match your system.

## Install and run

Clone the public repository into Waybar's configuration directory:

```bash
git clone https://github.com/xodo2fast4u/waybar.git ~/.config/waybar
waybar
```

If `~/.config/waybar` already exists, back up any files you want to keep before
cloning, or clone this repository elsewhere and copy `config.jsonc` and
`style.css` into that directory. To start the bar automatically, add `waybar`
to your Hyprland startup configuration.

## Customize

- Edit `config.jsonc` to change module placement, formats, intervals, click
  actions, and the clock timezone.
- Edit `style.css` to change colors, spacing, typography, and module appearance.
- The workspace configuration keeps workspaces 1–5 visible on all outputs.
  Change `persistent-workspaces` if you prefer a different set.
- CPU and memory clicks run `kitty -e btop`; the audio click runs `pavucontrol`.
  Change the relevant `on-click` values if you use different applications.
- The stylesheet includes battery selectors, but a battery module is not
  currently enabled in `config.jsonc`.

After editing the files, restart Waybar from your compositor or terminal if the
changes do not appear.

## Files

| File | Purpose |
| --- | --- |
| [`config.jsonc`](./config.jsonc) | Bar layout, modules, formats, and actions |
| [`style.css`](./style.css) | Colors, typography, and visual styling |

## License

See [`LICENSE`](./LICENSE).
