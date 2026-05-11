# Minesweeper

A terminal Minesweeper game built with the [notcurses](https://github.com/dankamongmen/notcurses) library.

## Requirements

- GCC (or compatible C11 compiler)
- notcurses development library

**Install notcurses:**
```bash
# Ubuntu / Debian
sudo apt install libnotcurses-dev

# Fedora
sudo dnf install notcurses-devel

# macOS
brew install notcurses
```

## Build

```bash
make
```

## Run

```bash
./minesweeper
```

## How to play

### Intro screen
Use **w / s** to move the selection up and down, then press **Enter** to confirm.

1. Choose a board size:
   - 9×9, 10 mines (Beginner)
   - 16×16, 40 mines (Intermediate)
   - 30×16, 99 mines (Expert)
   - Custom (enter your own rows, columns, mine count)

2. Choose a game variant:
   - **Normal** — standard Minesweeper
   - **Checkerboard** — the board alternates light and dark squares; mines on dark squares count as **2** toward neighboring cells' numbers
   - **The Liar** — displayed numbers are always off by ±1 (never below 0)

### During the game

| Key | Action |
|-----|--------|
| `w` / `↑` | Move cursor up |
| `s` / `↓` | Move cursor down |
| `a` / `←` | Move cursor left |
| `d` / `→` | Move cursor right |
| `c` | Clear (reveal) the cell under the cursor |
| `f` | Toggle flag on the cell under the cursor |
| `q` | Quit |

### Tips
- Your **first clear** is always safe — mines are placed after your first move.
- Flagging a cell decreases the **Remaining** mine counter even if the cell is not a mine.
- In Checkerboard mode, dark squares are slightly darker — plan accordingly!

## Features
- Color-coded numbers (1–8 each have a distinct color)
- Total mine count and remaining (unflagged) mine count always displayed
- Flood-fill auto-reveal for empty regions
- Three board size presets plus custom size
- Three game variants

## Clean

```bash
make clean
```