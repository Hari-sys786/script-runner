# ⚡ Script Runner v1.0 (Python)

Dark-themed desktop GUI for executing bash scripts from an Excel-driven menu.

## Features
- 🎨 Dark theme (Catppuccin Mocha)
- 📊 Reads `scripts.xlsx` — Category | Action | Script Path
- 🔗 Cascading dropdowns: Category → filters Actions
- ▶️ Execute scripts with real-time output streaming
- ■ Stop running scripts
- ↻ Reload Excel without restart
- 🧵 Background thread execution (UI stays responsive)

## Setup

```bash
pip install openpyxl

# Create sample Excel (optional)
python create_sample_excel.py

# Run
python script_runner.py
```

## Excel Format

Create `scripts.xlsx` in the same directory with 3 columns:

| Category | Action | Script Path |
|----------|--------|-------------|
| System | Check Disk Usage | /path/to/disk_usage.sh |
| System | Check Memory | /path/to/memory_check.sh |
| Network | Ping Test | /path/to/ping_test.sh |

- **Row 1** = Header (skipped)
- **Category** = Groups actions in first dropdown
- **Action** = Shows in second dropdown when category selected
- **Script Path** = Absolute path to bash script

## Requirements
- Python 3.6+
- tkinter (comes with Python)
- openpyxl (`pip install openpyxl`)
