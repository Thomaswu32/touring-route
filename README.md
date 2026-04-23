# Touring Route — Interactive Trip Maps

Self-hosted, interactive driving-route maps for multi-day road trips. Each route is a single `index.html` file — no build step, no framework, just open in a browser.

## Routes

| Folder | Trip | Days | Region |
|--------|------|------|--------|
| [`newmexicoroute/`](newmexicoroute/) | Southwest Slam | 8 days | TX → NM → CO |
| [`yellowstoneroute/`](yellowstoneroute/) | Yellowstone + Grand Teton | 7 days | UT → WY → MT |

## Features

- **Animated car marker** — click any day card and a 🚙 drives along the route polyline to that night's hotel
- **Interactive map** — OpenStreetMap via Leaflet; hotel markers geocoded automatically in the background
- **Spot tags** — clickable badges that link directly to 小红书 search results for each attraction
- **Edit mode** — in-browser editor lets anyone on the trip update the itinerary (day titles, highlights, hotel info, spot tags). Changes persist to Firebase (New Mexico) or localStorage (Yellowstone)
- **Mobile friendly** — viewport-locked layout works on phones and tablets

## Tech Stack

- [Leaflet.js](https://leafletjs.com/) — map rendering and markers
- [OpenStreetMap](https://www.openstreetmap.org/) tiles
- [Nominatim](https://nominatim.org/) — free geocoding for hotel addresses
- Firebase Realtime Database (New Mexico route) / `localStorage` (Yellowstone route)
- Vanilla JS, no build tooling

## Usage

Open any `index.html` directly in a browser — no server required for the Yellowstone route. The New Mexico route needs Firebase credentials already embedded in the file.

```
touring_route/
├── newmexicoroute/
│   └── index.html      # Firebase-backed, real-time sync across devices
└── yellowstoneroute/
    └── index.html      # localStorage, works fully offline
```

## Yellowstone Route Overview (May 2026)

```
Day 0  May 12  SLC ✈️ → Jackson WY                  ~4h drive
Day 1  May 13  Grand Teton NP (Oxbow Bend · Jenny Lake · Moose-Wilson)
Day 2  May 14  Enter Yellowstone → Grand Prismatic → Old Faithful → West Yellowstone
Day 3  May 15  Norris Basin → Mammoth Hot Springs → Lamar Valley (Red Dogs 🦬)
Day 4  May 16  Hayden Valley (grizzly window) → Mud Volcano → Grand Canyon of YS
Day 5  May 17  Lamar Valley farewell → Firehole Lake & Canyon Drive
Day 6  May 18  West Yellowstone → Idaho Falls → SLC ✈️
```

**Practical notes:** Year pass ($80/car) covers both Grand Teton + Yellowstone. Park at Fairy Falls Trailhead (not the main lot) for the Grand Prismatic overlook. Download Geyser Times app before entering the park.

## New Mexico Route Overview (Mar–Apr 2026)

```
Day 1  Mar 28  DFW land → Hurst TX
Day 2  Mar 29  Fort Worth Stockyards → Cadillac Ranch → Amarillo
Day 3  Mar 30  Amarillo → Santa Fe → Taos
Day 4  Mar 31  Great Sand Dunes → Durango CO
Day 5  Apr 01  Mesa Verde → Shiprock → Valley of Dreams → Farmington
Day 6  Apr 02  Farmington → ABQ → White Sands → El Paso
Day 7  Apr 03  El Paso → Carlsbad Caverns → Roswell → Abilene
Day 8  Apr 04  Abilene → Dallas Southlake
```
