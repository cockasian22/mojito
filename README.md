# 🍹 mojito

A beautifully simple, zero dependency, fresh file change monitoring tool. Monitor file changes in real time with ease using Mojito🍹!

## Features 🌿

- **Pixel-perfect alignment** of before/after columns
- **Color-coded changes** (green/+ adds, red/- removes, yellow/~ changes)
- **Per-change timestamps** (optional)
- **Zero dependencies** (pure Python stdlib)
- **Cross-platform** (Windows/macOS/Linux)

## Installation

### From PyPI
```bash
pip install mojito-watcher
```

### From Source
```bash
git clone https://github.com/yourusername/mojito.git
cd mojito
pip install -e .
```

## Usage

```bash
mojito path/to/file.txt [interval] [options]
```

### Options
| Flag               | Description                          | Default |
|--------------------|--------------------------------------|---------|
| `--no-color`       | Disable colored output               | Enabled |
| `--no-timestamps`  | Hide change timestamps               | Enabled |
| `[interval]`       | Polling interval in seconds          | 1.0     |

## Log to file

Just use the standart stdout to file
```bash
mojito path/to/file.txt > mojito.log
```

### Examples
```bash
# Basic usage
mojito config.yml

# Fast polling (0.5s) without colors
mojito script.py 0.5 --no-color

# Monitor JSON changes with timestamps
mojito data.json --no-timestamps
```

## Output Format

```
BEFORE                          │ AFTER
────────────────────────────────┼────────────────────────────────
unchanged_line                  │ unchanged_line
[14:30:45] old_value           ~> new_value
[14:30:46] deleted_line         - 
[14:30:47]                      + added_line
```

