# Old Computer — Typora themes

Green-screen word processor themes for Typora. Monospace text, one text
size, headings marked by `#` in the margin, inverse-video selection and
status bar, faint scanlines and a phosphor glow. Focus mode dims every
paragraph except the one you are writing to a darker shade of the same
phosphor, so the surrounding text stays legible but recedes.

## Variants

| File | Look |
| --- | --- |
| `old-computer-green.css` | P1 green phosphor (IBM 5151, Apple II) |
| `old-computer-amber.css` | P3 amber phosphor (Hercules, DEC VT220) |
| `old-computer-white.css` | White phosphor / monochrome monitor |
| `old-computer-blue.css` | WordPerfect 5.1 grey-on-blue |

All four share `old-computer/base.css`; a variant is just a set of
colour variables.

## Install

Copy the four `old-computer-*.css` files and the `old-computer` folder
into Typora's theme folder, then restart Typora and choose the theme
under Preferences → Appearance (or the Themes menu).

Theme folder locations:

- Linux: `~/.config/Typora/themes/`
- macOS: `~/Library/Application Support/abnerworks.Typora/themes/`
- Windows: `%APPDATA%\Typora\themes\`

Typora lists the themes as "Old Computer Green", "Old Computer Amber",
and so on.

## Tweaks

Edit the variant file (or add a `base.user.css` alongside it) and
override any of these variables in `:root`:

| Variable | Default | What it does |
| --- | --- | --- |
| `--crt-font` | IBM Plex Mono, JetBrains Mono, … monospace | Editor and UI font |
| `--crt-font-size` | `17px` | Base text size |
| `--crt-line-height` | `1.7` | Line spacing |
| `--crt-columns` | `84ch` | Maximum text width, in characters |
| `--crt-scanline` | `0.10` | Scanline darkness; `0` turns them off |
| `--crt-glow-radius` | `6px` | Phosphor glow; `0` turns it off |
| `--crt-image-filter` | `none` | CSS filter for images, e.g. `grayscale(1)` |

Colour roles used by every variant:

| Variable | Role |
| --- | --- |
| `--crt-bg` | Page background |
| `--crt-bg-alt` | Sidebar, code blocks, menus |
| `--crt-fg` | Body text |
| `--crt-bright` | Bold, headings, emphasis |
| `--crt-dim` | Markdown syntax, metadata, unfocused text in focus mode |
| `--crt-faint` | Borders and rules |
| `--crt-glow` | Glow colour (rgba) |
| `--crt-highlight` | Active line and hovered table rows (rgba) |

Printing and PDF export switch to black on white automatically.

## Making a new colour

Copy one of the variant files, rename it `old-computer-<name>.css`, and
change the eight colour variables. Keep `--crt-dim` legible against
`--crt-bg`: it is the colour of everything except the current paragraph
in focus mode.
