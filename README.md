# Latitude

A single-file web app that visualizes temperature differences around any latitude line on Earth.

![Single File](https://img.shields.io/badge/single_file-HTML-orange) ![License](https://img.shields.io/badge/license-MIT-blue)

---

## Features

| Feature | Description |
|---------|-------------|
| 🗺️ **Free Pan** | Drag anywhere on the map — full latitude and longitude movement |
| ⊙ **Set** | Drop a pin at the current center and load temperature data |
| ⌖ **Me** | Jump to your current location via geolocation |
| °C/°F **Toggle** | Switch between Celsius and Fahrenheit |
| 📊 **Area Chart** | Filled visualization showing temperature deviation from baseline |
| 🏷️ **Smart Labels** | Each point shows actual temp + difference (e.g., `15° ↑3`) |
| 🔗 **Shareable URLs** | `?lat=52.52&lon=13.4` links directly to any location |
| 📱 **Mobile Ready** | Touch-optimized with large tap targets |

---

## How It Works

1. **Pan the map** to any location you're curious about
2. **Tap "⊙ Set"** to drop a pin and fetch temperatures
3. **Explore the visualization** — the filled chart shows temperature differences across your latitude
4. **Check the legend** — see your temp, warmest point, and coldest point

---

## Temperature Visualization

The app samples temperature at **72 points** around your latitude (every 5° longitude) and draws:

- A **gray baseline** at your selected latitude
- **Filled areas** that rise (red) or dip (blue) based on temperature difference
- A **white line** tracing the actual temperature values
- **Labels** positioned outside the filled areas showing `temp° ↑/↓diff`

The vertical scale is 0.1° latitude per 1°C temperature difference.

---

## Tech

| Component | Choice |
|-----------|--------|
| Architecture | Single HTML file (~290 lines) |
| Maps | Leaflet.js (CDN) |
| Tiles | OpenFreeMap Dark via MapLibre GL (no key required) |
| Weather Data | Open-Meteo API (free, no key required) |
| Build Step | None |

---

## Example Locations

| Latitude | Location | What You'll See |
|----------|----------|-----------------|
| `52.52` | Berlin | Central Europe → Canada → Russia |
| `40.71` | New York | Mediterranean → Japan → Spain |
| `35.68` | Tokyo | Subtropics → Los Angeles → Sahara |
| `-33.87` | Sydney | Southern hemisphere → Cape Town → Buenos Aires |
| `0` | Equator | Tropical belt around the world |



## Deploy

Works on any static host:

**GitHub Pages:**
1. Push to GitHub
2. Settings → Pages → Deploy from `main` branch
3. Done!
