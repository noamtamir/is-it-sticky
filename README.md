# Is it sticky?

A simple weather app that tells you if it feels sticky in your location. 

## How it works?
1. Requests your location via the browser
2. Fetches weather data with open-meteo API 
3. Tells you if it's sticky from the temperature and dew point:
   - At 25°C or below: not sticky
   - Above 25°C with a dew point below 16°C: not sticky
   - Above 25°C with a dew point from 16°C through 18°C: kinda sticky
   - Above 25°C with a dew point above 18°C through 21°C: sticky
   - Above 25°C with a dew point above 21°C: very sticky

## Install as an app
The app is installable from a modern mobile browser when served over HTTPS (or from
`localhost` during development). On Android, use the browser's **Install app** or
**Add to Home screen** option. On iPhone, use Safari's **Share → Add to Home Screen**.

The service worker stores the app shell for offline startup. Live weather and location
data still require a network connection and location permission.

## Development

No dependencies or build process are required. Serve the project locally to test PWA
features:

```sh
python3 -m http.server 8000
```
