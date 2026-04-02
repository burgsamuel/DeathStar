# Death Star Tracker

Real-time International Space Station (ISS) orbital tracker with a Star Wars twist. The ISS is represented as the Death Star, accompanied by animated X-Wing and Millennium Falcon markers flying across the map.

![Death Star Tracker Screenshot](https://github.com/user-attachments/assets/7b832ee8-9dbe-4edf-9574-8799104ad3c2)

## Features

- **Real-Time ISS Tracking** — Displays live latitude, longitude, velocity, and altitude updated every 5 seconds
- **Death Star Marker** — The ISS appears as the Death Star on a dark-themed world map
- **Animated Companions** — X-Wing and Millennium Falcon markers animate along the map
- **Orbit Visualization** — Dashed polyline shows the projected orbital path
- **Find Death Star Button** — Re-centers the map on the current ISS position
- **Dark Theme UI** — Sleek dark interface styled with Tailwind CSS

## How It Works

The app fetches live telemetry from the [Where Is The ISS](https://wheretheiss.at/w/developer) API and plots the position on an interactive Leaflet.js map. Orbit track points are fetched in batches to draw the upcoming trajectory.

## Technologies

- **HTML / CSS / JavaScript** — Single-file app, no build step required
- **Leaflet.js** — Interactive map rendering
- **Tailwind CSS** — Utility-first styling via CDN
- **Where Is The ISS API** — Open ISS telemetry data

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/DeathStar.git
   ```
2. Open `index.html` in any modern browser.

No dependencies to install, no build process — it just works.

## API Reference

Uses the public [Where Is The ISS API](https://wheretheiss.at/w/developer):

| Endpoint | Description |
|----------|-------------|
| `GET /v1/satellites/25544` | Current ISS position, velocity, and altitude |
| `GET /v1/satellites/25544/positions?timestamps=...` | Predicted positions for orbit track |

## License

This project is open source. Use it however you like.

## Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.
