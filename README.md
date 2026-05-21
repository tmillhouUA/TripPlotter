# Trip Plotter V1.0

A browser-based tool for creating custom travel maps. Design multi-trip itineraries on an interactive Mercator map, then export plotter-friendly SVG files (paths only, interpolated curves).

## Features

- **Multiple trips** — create any number of named, color-coded trips on a single map
- **Great-circle and road routing** — flight legs follow geodesic paths; road legs fetch real driving routes
- **Destination markers** — mark waypoints as destinations with auto-placed, nudgeable Hershey-font labels
- **Adjustable map extent** — shift + click + drag a bounding box or type coordinates to frame any region
- **Adjustable map content** — multiple map layers and per-country content via right-click context menus
- **Layer controls** — toggle and style coastlines, borders, rivers, lakes, graticule, geographic lines, major highways, and secondary roads independently
- **Plot mode** — lock the view to exact paper dimensions (inches or cm) for precise SVG export
- **Save / load projects** — export and reimport `.tprj` project files to resume work across sessions; export individual trips (or sets of trips) to transfer between projects
- **Variable graphics detail** — work on a low-res map for older machines
- **No server required** — runs entirely in the browser; all data is bundled locally

## Usage

Open `index.html` in any modern browser. No build step or internet connection is required for core functionality--includes flight paths and basic city search. Road routing and city search make external API calls (see Data Sources).

## Data Sources

| Data | Source |
|------|--------|
| Coastlines, borders, rivers, lakes, geographic lines | [Natural Earth](https://www.naturalearthdata.com/) (public domain) |
| Major and secondary road geometry | [Natural Earth](https://www.naturalearthdata.com/) (public domain) |
| Road routing (driving legs) | [OSRM](http://project-osrm.org/) — open-source routing engine using OpenStreetMap data |
| City name search | [Nominatim](https://nominatim.openstreetmap.org/) — geocoding API using [OpenStreetMap](https://www.openstreetmap.org/) data |
| Map labels (single-stroke font) | Hershey Simplex Roman — James Iro Hershey, 1967 (public domain); glyph data via [HersheyFonts](https://pypi.org/project/hersheyfonts/) |
