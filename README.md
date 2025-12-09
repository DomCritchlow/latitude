# Your Latitude, Every Longitude

🌍 **[Live Demo → critchlow.us/latitude](https://critchlow.us/latitude/)**

A minimal web app that draws your latitude line around the entire Earth, with real-time temperature data showing how warm or cold it is at every point along your parallel.

![Screenshot](https://img.shields.io/badge/single_file-HTML-orange)

---

## Features

| Feature | Description |
|---------|-------------|
| 📍 **Geolocation** | One tap to find your latitude |
| 🌡️ **Temperature Graph** | Live temps along your latitude — red (warmer than you), blue (colder) |
| ↕️ **Latitude Stepper** | Jump 5° north/south with arrow buttons |
| 🔄 **Horizontal Pan** | Drag left/right to explore your parallel |
| ⊙ **Center Tracking** | White dot + live longitude display as you pan |
| 🔗 **Shareable URLs** | `?lat=52.52` links directly to any latitude |
| 📱 **Mobile Friendly** | Touch-optimized with large tap targets |

---

## How It Works

1. **Pick your latitude** — type it in, use geolocation, or tap ↑/↓
2. **Explore horizontally** — drag to pan around the globe at that latitude
3. **See the temperature profile** — the line rises (red) where it's warmer than you, dips (blue) where it's colder
4. **Check the legend** — see your temp, global max/min, and current center longitude

---

## Tech Stack

- **Single HTML file** — no build step, no install
- **Leaflet.js** — reliable map rendering (CDN)
- **Open-Meteo API** — free weather data, no API key
- **CartoDB Dark Matter** — stylish dark map tiles

---

## Temperature Visualization

The app samples temperature at 24 points around your latitude (every 15° longitude) and draws a line that:

- **Sits on your latitude** at your location (baseline)
- **Rises above** where it's warmer than you (red)
- **Dips below** where it's colder than you (blue)
- **Labels each point** with the actual temperature

---

## Example Latitudes

| Latitude | Location | What You'll See |
|----------|----------|-----------------|
| `52.52` | Berlin | Central Europe, crosses Canada, Russia |
| `40.71` | New York | Mediterranean, crosses Japan, Spain |
| `35.68` | Tokyo | Subtropics, crosses Los Angeles, Sahara |
| `-33.87` | Sydney | Southern hemisphere, Cape Town, Buenos Aires |
| `0` | Equator | Tropical belt around the world |

---

## Local Development

Just open `index.html` in a browser. Or serve it:

```bash
python3 -m http.server 8080
# Open http://localhost:8080
```

---

## Deployment

Works on any static host. For GitHub Pages:

1. Push to GitHub
2. Settings → Pages → Deploy from `main` branch
3. Done!
