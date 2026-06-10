# Weather Dashboard

A modern, responsive weather dashboard that fetches real-time weather data using the **Open-Meteo API** (free, no API key required).

## Features

✨ **Current Weather Display**
- Real-time temperature and weather conditions
- Humidity, wind speed, pressure, visibility
- Feels-like temperature
- Geographic coordinates
- Weather emoji icons

⏰ **Hourly Forecast**
- 24-hour forecast with hourly temperature
- Weather conditions for each hour
- Interactive cards with hover effects

📅 **7-Day Forecast**
- Daily high and low temperatures
- Weather conditions for each day
- Visual card layout with weather emojis

🔍 **City Search**
- Search for any city in the world
- Powered by Nominatim (OpenStreetMap)
- Auto-complete ready

📱 **Responsive Design**
- Works on desktop, tablet, and mobile
- Touch-friendly interface
- Optimized loading states

## APIs Used

### 1. Open-Meteo API
- **URL:** https://api.open-meteo.com/v1/forecast
- **Free:** Yes, no API key required
- **Rate Limit:** 10,000 requests/day
- **Data:** Current weather, hourly, and 7-day forecast

### 2. Nominatim (OpenStreetMap)
- **URL:** https://nominatim.openstreetmap.org/search
- **Free:** Yes, no API key required
- **Use:** Geocoding city names to coordinates

## How It Works

1. **Search Input:** User enters a city name
2. **Geocoding:** Nominatim converts city name to latitude/longitude
3. **Weather Fetch:** Open-Meteo API retrieves weather data
4. **Display:** Data is rendered in real-time

## Installation

1. Save the HTML file as `weather-dashboard.html`
2. Open in any modern browser
3. Start searching for cities!

## Usage

```html
<!-- Simply open the file -->
open weather-dashboard.html
```

## Code Structure

### Key Functions

```javascript
// Geocode city name to coordinates
geocodeCity(cityName) → { name, latitude, longitude }

// Fetch weather data from Open-Meteo
fetchWeather(latitude, longitude, cityName) → weatherData

// Display current weather information
displayCurrentWeather(data)

// Display hourly forecast
displayHourlyForecast(data)

// Display 7-day forecast
displayDailyForecast(data)
```

### Weather Code Mapping

Weather codes (WMO) are converted to:
- Emoji icons (☀️, ⛅, 🌧️, ❄️, ⛈️, etc.)
- Descriptions (Clear sky, Partly cloudy, Rain, etc.)

## Customization

### Change Default City

Edit the last line in the script:
```javascript
cityInput.value = 'Tokyo'; // Change to any city
```

### Change Color Scheme

Edit CSS variables:
```css
:root {
  --primary: #1e3a8a;      /* Dark blue */
  --secondary: #3b82f6;    /* Light blue */
  --accent: #60a5fa;       /* Accent blue */
  /* ... */
}
```

### Change Temperature Units

Modify the API URL query (add `&temperature_unit=fahrenheit`):
```javascript
// For Fahrenheit
`https://api.open-meteo.com/v1/forecast?...&temperature_unit=fahrenheit`
```

## Browser Support

- ✅ Chrome/Edge 88+
- ✅ Firefox 85+
- ✅ Safari 14+
- ✅ Mobile browsers

## API Response Example

```json
{
  "current": {
    "temperature_2m": 22.5,
    "relative_humidity_2m": 65,
    "weather_code": 2,
    "wind_speed_10m": 12.4,
    "pressure_msl": 1013,
    "visibility": 10000
  },
  "hourly": {
    "time": [...],
    "temperature_2m": [...],
    "weather_code": [...]
  },
  "daily": {
    "time": [...],
    "temperature_2m_max": [...],
    "temperature_2m_min": [...],
    "weather_code": [...]
  }
}
```

## Error Handling

- Invalid city name → Shows error message
- Network error → Shows error message
- Auto-hides error after 5 seconds
- Loading spinner during data fetch

## Performance

- Single-page application (no page reload)
- API calls cached per search
- Minimal DOM manipulation
- Optimized CSS animations

## Future Enhancements

- Add location geolocation (GPS)
- Weather alerts and warnings
- Multiple city comparison
- Rainfall and UV index
- Historical weather data
- Export as PDF
- Dark/light theme toggle

## License

Free to use and modify.

## References

- [Open-Meteo Documentation](https://open-meteo.com/)
- [Nominatim Documentation](https://nominatim.org/)
- [WMO Weather Codes](https://www.weather.gov/media/epz/wxcalc/rhTdFromWetBulb.pdf)
