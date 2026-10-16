# 🐠 JBL ProScan Lovelace Card

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE)
[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-2026.3%2B-41BDF5.svg?style=flat-square&logo=homeassistant)](https://www.home-assistant.io/)
[![HACS Custom](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=flat-square)](https://hacs.xyz/)
[![Maintainer](https://img.shields.io/badge/Maintainer-AuroreVgn-blue.svg?style=flat-square)](https://github.com/AuroreVgn)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-Soutenir-FF5E5B?logo=kofi&logoColor=white&style=flat-square)](https://ko-fi.com/aurorevgn)

## 🌍 Other languages

[Français](README.md)

## 🏠 My Home Assistant Projects

Discover all my Home Assistant integrations and projects on my dedicated page: [**🏠 Discover my Home Assistant Projects**](https://erra.me)

## ☕ Support the project

If you find this integration useful and would like to support its development and maintenance:

<p>
  <a href="https://ko-fi.com/aurorevgn">
    <img src="https://storage.ko-fi.com/cdn/kofi4.png?v=3"
         alt="Support me on Ko-fi"
         height="45">
  </a>
</p>

## 📑 Table of contents

- [⚠️ Important](#-important)
- [✨ Features](#-features)
- [📦 Installation](#-installation)
- [⚙️ Configuration](#-configuration)
- [🎛️ Water quality thresholds](#-water-quality-thresholds)
- [📸 Previews](#-previews)
- [🎨 Visual Editor](#-visual-editor)
- [📈 Interactive Dashboard](#-interactive-dashboard)
- [⚙️ Customization](#-customization)
- [🧩 Companion Integration](#-companion-integration)
- [📄 License](#-license)

## ⚠️ Important


A modern Lovelace card for the **JBL ProScan** Home Assistant integration.

➡️ **Integration available here:** https://github.com/AuroreVgn/JBL_ProScan

## ✨ Features
- 🎨 Mushroom-inspired design
- 📱 Fully responsive
- 🌍 Multi-language support (🇫🇷 🇬🇧 🇩🇪 🇪🇸 🇮🇹 🇳🇱 🇵🇹)
- 🧩 Native Home Assistant visual editor
- 🌞 Light & Dark theme support
- 🔄 Manual refresh button
- 📊 Interactive history graph
- 📈 Home Assistant Long-Term Statistics support
- 📅 History period selector
- 🔍 Interactive tooltips
- 📉 JBL recommended ranges
- 🔄 Previous analysis comparison
- 🎨 Native Home Assistant color picker
- 🎭 Native Home Assistant icon picker
- ⚙️ Highly customizable

## 📦 Installation

### HACS (recommended)

#### Add to HACS

##### Automatically
[![Open your Home Assistant instance and open this repository in HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=AuroreVgn&repository=JBL_ProScan_card&category=plugin)

##### Manually
```
HACS
 └── Dashboards
      └── ⋮
           └── Custom repositories

Repository
https://github.com/AuroreVgn/JBL_ProScan_card

Category
Dashboard
```

#### Download
```
HACS
 └── JBL ProScan Card
      └── Download
```

Restart Home Assistant if requested.


## ⚙️ Configuration
Minimal configuration:

```yaml
type: custom:jbl-proscan-card
entity: sensor.bassin_historique
```

If your history sensor has a different entity ID, simply replace:

```yaml
sensor.bassin_historique
```
with your own sensor.


## 🎛️ Water quality thresholds

Each measurement and each point on the history chart is colored individually
according to the thresholds below.

> Values exactly equal to the lower or upper limit of the recommended range
> are considered within the recommended range and are therefore displayed in 🟢 green.

| Parameter | 🟢 Good | 🟠 Warning | 🔴 Poor |
|---|---|---|---|
| **pH** | 6.5 ≤ pH ≤ 8.5 | 6.0 ≤ pH < 6.5 or 8.5 < pH ≤ 9.0 | pH < 6.0 or pH > 9.0 |
| **KH** | 5 ≤ KH ≤ 15 °dKH | 3 ≤ KH < 5 or 15 < KH ≤ 20 °dKH | KH < 3 or KH > 20 °dKH |
| **GH** | 4 ≤ GH ≤ 21 °dGH | 2 ≤ GH < 4 or 21 < GH ≤ 28 °dGH | GH < 2 or GH > 28 °dGH |
| **NO₂** | 0 ≤ NO₂ ≤ 0.25 mg/L | — | NO₂ > 0.25 mg/L |
| **NO₃** | NO₃ ≤ 25 mg/L | 25 < NO₃ ≤ 50 mg/L | NO₃ > 50 mg/L |
| **CO₂** | Information only | — | — |
| **Chlorine** | 0 ≤ Chlorine ≤ 0.8 mg/L | — | Chlorine > 0.8 mg/L |

## 📸 Previews

| Light mode | Dark and compatct mode|
| :---: | :---: |
| ![JBL ProScan Card — light mode](assets/light.png) | ![JBL ProScan Card — dark mode](assets/dark.png) |

## 🎨 Visual Editor
The card fully supports the Home Assistant visual editor.

Available options include:
- Title
- History length
- Number of displayed measurements
- Compact mode
- Show / hide CO₂
- Water quality thresholds
- Manual refresh button
- History period selector
- Custom colors
- Custom icons
- Recommended JBL ranges

No YAML editing required for most users.


## 📈 Interactive Dashboard
The card provides:
- 📊 Water quality overview
- 📈 Historical charts
- 📅 Selectable periods
  - 1 month
  - 3 months
  - 1 year
  - All history
- 🔄 Manual refresh
- 📉 Comparison with the previous analysis
- 📍 JBL recommended ranges
- 🖱 Rich interactive tooltips
- 📊 Home Assistant statistics support

## ⚙️ Customization
The appearance can be customized directly from the visual editor.

### Colors
- Accent color
- Good
- Warning
- Critical
(using the native Home Assistant color picker)

### Icons
Customize every icon using the native Home Assistant icon picker:
- Header
- Refresh
- pH
- KH
- GH
- NO₂
- NO₃
- CO₂
- Chlorine

## 🧩 Companion Integration
This card requires the **JBL ProScan** integration.
➡️ https://github.com/AuroreVgn/JBL_ProScan


## 📄 License
Distributed under the MIT License.

[releases-shield]: https://img.shields.io/github/v/release/AuroreVgn/JBL_ProScan_card?style=flat-square
[releases]: https://github.com/AuroreVgn/JBL_ProScan_card/releases
[license-shield]: https://img.shields.io/github/license/AuroreVgn/JBL_ProScan_card?style=flat-square
