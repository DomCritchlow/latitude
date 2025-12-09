# Your Latitude, Every Longitude

A minimal web app that draws your latitude line around the entire Earth. Pan left and right to explore what shares your parallel.

![Demo](https://img.shields.io/badge/demo-live-brightgreen)

## Features

- 📍 **Geolocation** — Click to find your latitude instantly
- 🌍 **Infinite scroll** — Pan horizontally around the globe
- 📐 **Latitude line** — See your exact parallel drawn across the map
- 🔗 **Shareable URLs** — `?lat=48.77` links directly to any latitude
- 🎨 **Dark theme** — CartoDB Dark Matter tiles

## Usage

1. Open `index.html` in a browser
2. Click 📍 to use your location, or type a latitude
3. Drag left/right to explore your latitude line

## Tech

- **Single HTML file** — No build step, no dependencies to install
- **Leaflet.js** — Loaded from CDN for reliable map rendering
- **~70 lines** — Minimal, readable code

## How It Works

The map is locked to a fixed zoom level with vertical panning disabled. A polyline is drawn at your latitude extending far beyond the map bounds, creating the illusion of an infinite latitude line.

## Examples

| Latitude | Location |
|----------|----------|
| `48.77` | Stuttgart, Germany |
| `40.71` | New York City |
| `35.68` | Tokyo |
| `-33.87` | Sydney |
| `0` | Equator |

## License

MIT

