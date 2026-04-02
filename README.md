# Death Star Tracker

A Star Wars-themed real-time ISS (International Space Station) orbital tracker built as a single-page web application.

![Death Star Tracker](https://img.shields.io/badge/status-active-brightgreen)

## Features

- **Real-Time ISS Tracking** — Displays the current latitude, longitude, velocity, and altitude of the ISS
- **Interactive Map** — Dark-themed Leaflet map with live orbital position updates every 5 seconds
- **Orbit Path Visualization** — Draws the projected ISS orbit track with dashed polylines
- **Animated Star Wars Icons** — X-Wing and Millennium Falcon markers that traverse the map
- **One-Click Locate** — "Find Death Star Now!" button recenters the map on the ISS

## Tech Stack

- **HTML / CSS / JavaScript** — Single-file app, no build step required
- [Tailwind CSS](https://tailwindcss.com/) — Utility-first styling (via CDN)
- [Leaflet](https://leafletjs.com/) — Interactive map rendering
- [WhereTheISS.at API](https://wheretheiss.at/) — Real-time ISS telemetry data
- **CartoDB Dark Tiles** — Dark basemap for the map

## Getting Started

No installation or build process needed. Just open the file in a browser:

```bash
open index.html
```

Or serve it locally:

```bash
npx serve .
# then visit http://localhost:3000
```

## How It Works

1. On load, the app fetches the ISS position from `api.wheretheiss.at`
2. The map centers on the ISS and a marker tracks its movement
3. Every 5 seconds, the ISS position updates (lat, lon, velocity, altitude)
4. Every 5 minutes, the orbit track is recalculated and redrawn
5. X-Wing and Millennium Falcon icons animate independently across the map

## Project Structure

```
DeathStar/
├── index.html   # Entire application (HTML + CSS + JS)
└── README.md
```

## License

MIT
