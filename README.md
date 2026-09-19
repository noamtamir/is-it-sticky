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

## Single File
Everything is contained in `index.html` - no dependencies or build process required.
