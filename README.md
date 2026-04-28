# Elevation Symphony

Pick a path on a map of the USA. The app samples the elevation along the path and turns it into music — three octaves of chromatic notes, played as a soft yin (bamboo flute) tone from sea level up to 15,000 ft. Above 15,000 ft a brass horn takes over.

A glowing dot travels along the path on the map, changing color with elevation, while a rainbow elevation bar on the left shows the same elevation in real time.

## How to use

1. Open the live site (link below) or open `index.html` in a browser.
2. Click anywhere on the map to add waypoints — the dashed line is your path.
3. Drag waypoints to fine-tune. Use **Undo** / **Clear** to edit.
4. Set the **duration** (10 sec – 30 min) and **notes/sec** (2 / 4 / 8).
5. Tap **Sample Elevations**, then **Play**.

## Data + tech

- Map tiles: OpenTopoMap (CC-BY-SA)
- Elevation: Open-Meteo Elevation API (SRTM/Copernicus DEM, ~90m resolution, free, no key)
- Audio: Web Audio API (no audio files — fully synthesized)
- Map library: Leaflet

## Notes on coverage

- Continental USA: full coverage.
- Alaska: SRTM only goes to 60° N — the North Slope is interpolated/missing in some sources.
- For higher resolution USA-only data (1–10 m), USGS 3DEP is better but slower per query.

## Local dev

It's a single HTML file. Open it directly, or serve with any static server:

```
python -m http.server 8000
# or
npx serve .
```

No build step.
