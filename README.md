# Wien Öffis Live-Display

Single-file Web-App, die Wiener-Linien-Echtzeitdaten als Retro-Subway-Display anzeigt — gedacht für ein iPhone, das als permanentes Wand-Display dient.

## Features

- **4 Stationen** durchswipebar (U1 Reumannplatz · Tram 6 Quellenstraße · Tram 1 Knöllgasse · Bus 14A Sonnleithnergasse)
- Pro Station beide Richtungen mit den nächsten 3 Abfahrten
- Retro Dot-Matrix Look mit amber LED-Schrift und neon-grüner Analog-Uhr
- Auto-Refresh alle 20 Sekunden
- Funktioniert als PWA — "Zum Home-Bildschirm" für Fullscreen-Modus

## Installation auf dem iPhone

1. URL des deployten Sites in **Safari** öffnen (siehe GitHub Pages URL unten)
2. Teilen-Button → **"Zum Home-Bildschirm"**
3. iPhone in Landscape an die Wand → Icon antippen → läuft im Fullscreen

Optional: Geführter Zugriff aktivieren (`Einstellungen → Bedienungshilfen → Geführter Zugriff`), damit der Screen nicht versehentlich verlassen wird.

## Stationen anpassen

Direkt im `index.html` im `STATIONS` Array editieren. RBL-Nummern findest du im Wiener-Linien-OGD-Datensatz `wienerlinien-ogd-haltepunkte.csv` (data.wien.gv.at).

## Tech

- Single-file HTML, kein Build-Schritt
- Datenquelle: [Wiener Linien Echtzeit-Schnittstelle](https://www.wienerlinien.at/ogd_realtime/monitor) (CC-BY)
- CORS-Workaround über öffentliche Proxy-Kette (corsproxy.io, allorigins, codetabs, thingproxy, corsproxy.org)
- Fonts: VT323 + Press Start 2P via Google Fonts
- Wake-Lock-API für Always-On (iOS 16.4+)

## Deployment

Per GitHub Pages auf `main` Branch aktiviert — jeder Push deployed automatisch.
