# Rose Pine theme for `bat`

<p align="center">
  <img src="https://raw.githubusercontent.com/rose-pine/rose-pine-theme/main/assets/banner.png" alt="Rose Pine Banner" />
</p>

A calming, tasteful theme for the [`bat`](https://github.com/sharkdp/bat) syntax-highlighting pager, based on the delightful [Rose Pine](https://rosepinetheme.com) palette.

This repository provides a single Sublime Text `.tmTheme` file: `Rose-Pine.tmTheme`.

## Palette
| Name    | Hex     | Role |
|---------|---------|------|
| Base    | `#191724` | Background |
| Surface | `#1f1d2e` | Subtle background |
| Overlay | `#26233a` | Elevated background |
| Muted   | `#6e6a86` | Comments / subtle text |
| Subtle  | `#908caa` | Secondary text |
| Text    | `#e0def4` | Primary text |
| Love    | `#eb6f92` | Errors / deletions |
| Gold    | `#f6c177` | Constants / numbers |
| Rose    | `#ea9a97` | Strings / accents |
| Pine    | `#31748f` | Types / declarations |
| Foam    | `#9ccfd8` | Functions / methods |
| Iris    | `#c4a7e7` | Keywords / control |
| Highlight | `#524f67` | Selection / emphasis |

<p align="center">
  <img src="https://raw.githubusercontent.com/rose-pine/rose-pine-theme/main/assets/palette.png" alt="Rose Pine Palette" />
</p>

## Installation

### Option 1: Clone this repo
```bash
mkdir -p ~/.config/bat/themes
cd ~/.config/bat/themes
# Clone (or copy) the single theme file
curl -O https://raw.githubusercontent.com/aaron/rose-pine-bat/main/Rose-Pine.tmTheme
# (Alternatively: git clone this repository and copy Rose-Pine.tmTheme here)

# Rebuild bat's theme cache
bat cache --build
```

### Option 2: Copy directly from a local checkout
If you have this repository locally:
```bash
mkdir -p ~/.config/bat/themes
cp Rose-Pine.tmTheme ~/.config/bat/themes/
bat cache --build
```

## Usage

On the command line (one-off):
```bash
bat --theme "Rose-Pine" README.md
```

Persist via environment variable:
```bash
export BAT_THEME="Rose-Pine"
```
Add that line to your shell profile (`~/.bashrc`, `~/.zshrc`, etc.) to keep it.

Or add to `~/.config/bat/config`:
```
--theme=Rose-Pine
```

## Verification
List available themes:
```bash
bat --list-themes | grep -i rose
```
You should see `Rose-Pine`.

## Updating
Repeat the installation copy/curl step and run:
```bash
bat cache --clear
bat cache --build
```

## Notes
- `bat` consumes Sublime Text `.tmTheme` (XML) definitions; this file maps Rose Pine palette colors to common scopes.
- If future palette adjustments occur upstream, update the hex values accordingly.

## Contributing
Feel free to open issues or PRs to refine scope mappings (e.g. adjusting punctuation, diff colors, or diagnostics).

## License
Rose Pine palette and name are © Rose Pine authors. This theme file follows the upstream license conventions; see Rose Pine project for details. The `bat` utility is © sharkdp and contributors.

<p align="center">
  <img src="https://raw.githubusercontent.com/rose-pine/rose-pine-theme/main/assets/icon.png" alt="Rose Pine Icon" width="96" />
</p>
