# Time.N.Weather — Dashboard Wiki

A global time and weather dashboard for tracking live local times, current conditions, hourly/daily forecasts, and deep astronomical data for any city on Earth. Built for the **Vivaldi Browser Side Panel** and the Vivaldi Community, and works as a standalone page in any modern desktop or mobile browser.

**Repository:** [github.com/ggr03/Time.N.Weather-Dashboard](https://github.com/ggr03/Time.N.Weather-Dashboard)

---

## Table of Contents

1. [Managing Your Cities](#1-managing-your-cities)
2. [The Four Weather Views](#2-the-four-weather-views)
3. [Reading Local Weather Information](#3-reading-local-weather-information)
4. [24-Hour & 7-Day Forecasts](#4-24-hour--7-day-forecasts)
5. [Reading Lunar Metrics & Lighting Stats](#5-reading-lunar-metrics--lighting-stats)
6. [Language Support](#6-language-support)
7. [Mobile & Cross-Browser Support](#7-mobile--cross-browser-support)
8. [Data Persistence](#8-data-persistence)
9. [Troubleshooting](#9-troubleshooting)
10. [Credits & License](#10-credits--license)

---

## 1. Managing Your Cities

The dashboard tracks multiple locations worldwide, each with its own local timezone and localized weather data. Everything is stored in your browser — there's no account and no server-side sync.

### Adding a New City

The dashboard uses a live, high-precision geocoding API to find exact global locations.

1. Locate the **Search Bar** at the top of the sidebar.
2. Begin typing the name of a city (a minimum of 2 characters is required before results appear).
3. **Wait a brief moment.** A dropdown will populate with matches from the global database, showing the city, region/state, and country to help you tell apart places that share a name (e.g., *London, England* vs. *London, Ontario, Canada*).
4. Select the correct city from the dropdown list.
5. Click **"Add City"** (or press `Enter`). The city appears as a new tab in your sidebar, and its panel shows just the plain city name — the region/country shown in the search dropdown is only there to help you pick the right match.

> **Tip:** If you add a city that's already in your list, the dashboard simply switches to its existing tab instead of creating a duplicate.

### Rearranging Cities

Reorder your saved cities with native drag-and-drop:

1. **Hover** over any city tab you want to move — the cursor changes to a "grab" hand.
2. **Click and hold** the tab; it becomes slightly transparent to show it's being dragged.
3. **Drag** it up or down the list. A dashed blue border marks exactly where it will land as you pass over other tabs.
4. **Release** to drop it into place. The new order is saved automatically.

*(When you click a tab to view its weather, it "pops up" with a 3D shadow to mark it as the active view. Unselected tabs stay flat.)*

### Removing a City

Each tab has a small **✕** close button in its corner. Tapping/clicking it removes that city from your list immediately (no confirmation prompt), and updates your saved list.

---

## 2. The Four Weather Views

Once a city is selected, four view toggles sit at the top of the main panel:

| View | What it shows |
|---|---|
| **Local Weather** | Current conditions bento-grid — temperature, sun/moon times, solar position, AQI, humidity, wind, pressure, UV, and pollutants |
| **24-Hour Forecast** | Hour-by-hour conditions and temperature for the next 24 hours, starting from the current hour |
| **7-Day Forecast** | Daily high/low temperatures and conditions for the coming week |
| **Lunar Metrics** | Moon phase, illumination, distance, upcoming full/new moon dates, and photography-focused lighting data (blue hour, golden hour, twilights) |

Every temperature throughout the dashboard is shown in **both Celsius and Fahrenheit** side by side, so you never need to switch units.

---

## 3. Reading Local Weather Information

The **Local Weather** view presents a "bento-box" grid of current meteorological conditions:

- **Condition & Temp:** Current weather icon (e.g., ⛅ Partly Cloudy), air temperature in °C/°F, and "Feels like" (apparent) temperature factoring in humidity and wind chill.
- **Sunrise & Sunset:** Local times the sun crests the horizon (🌅) and disappears (🌇).
- **Moonrise & Moonset:** Local times the moon appears (🌛) and sets (🌜) for that city.
- **Solar Position:**
  - *Noon / Nadir:* When the sun reaches its highest point (Solar Noon) and lowest point beneath the earth (Nadir).
  - *Azimuth:* Compass direction of the sun, in degrees.
  - *Altitude:* Height of the sun above the horizon, in degrees.
- **Day & Night Length:** Total daylight (☀️) versus total darkness (🌙) for the current 24-hour cycle.
- **Air Quality (AQI):** Current US Air Quality Index score. Color-codes from green to purple across Good, Moderate, Unhealthy for Sensitive Groups, Unhealthy, Very Unhealthy, and Hazardous.
- **Pollutants:** Dust concentration (µg/m³), alongside NO₂ and other pollutant data feeding into the AQI score.
- **Humidity & Dewpoint:** Water vapor percentage in the air, paired with the temperature at which dew forms — a good indicator of how "muggy" the air feels.
- **Wind Speed:** Current sustained wind speed.
- **Air Pressure:** Atmospheric surface pressure in hectopascals (hPa).
- **Max UV Index:** Predicted peak ultraviolet radiation for the day.
- **Visibility:** Current visibility, categorized as Clear, Reduced, or Poor.

---

## 4. 24-Hour & 7-Day Forecasts

- **24-Hour Forecast:** Lists conditions hour by hour starting from right now, with icon, short description, and temperature (°C/°F) for each hour. Scrolls independently of the rest of the page.
- **7-Day Forecast:** One row per day, showing the day/date, a summary icon and condition, and the day's high (↑) and low (↓) temperatures in °C and °F.

Both lists pull from the same live forecast data as the Local Weather view, so they always stay in sync with the selected city.

---

## 5. Reading Lunar Metrics & Lighting Stats

Selecting **Lunar Metrics** swaps in advanced astronomical data calculated from the exact latitude and longitude of your selected city.

### The Lunar Bento Cards

- **Moon Phase:** Icon plus astronomical name of the current phase (e.g., *Waxing Crescent*, *Waning Gibbous*).
- **Illumination:** Percentage of the moon's surface currently lit and visible from Earth.
- **Earth Distance:** Real-time geocentric distance between Earth and the Moon, in kilometers.
- **Next Full Moon / Next New Moon:** Upcoming calendar dates for 100% illumination (Full) and 0% illumination (New).
- **Moon Age:** Days elapsed since the last New Moon, tracking progress through the ~29.5-day synodic cycle.

### The Lighting Grid (Photography & Civil Data)

The Morning and Evening Lighting panels track specific solar angles beneath the horizon that dictate light quality for photography and civil twilight phases:

- **Blue Hour:** Sun between -8° and -4° below the horizon — a deep blue sky, ideal for landscape and city photography.
- **Golden Hour:** Sun between -4° below and +6° above the horizon — soft, warm light favored by photographers.
- **Twilights:**
  - *Astronomical Twilight:* Sun -18° to -12° below the horizon. Darkest phase; stars fully visible, horizon barely distinguishable.
  - *Nautical Twilight:* Sun -12° to -6° below the horizon. Horizon visible; sailors can navigate by stars.
  - *Civil Twilight:* Sun -6° to 0° below the horizon. Brightest twilight; enough natural light for outdoor activities without artificial lighting.

---

## 6. Language Support

Below the city search bar, a dropdown menu displays your active language (e.g., "English"). The full UI — labels, weather condition text, and date/time formatting — translates instantly on selection, with no page reload. Languages are grouped by region:

- **European:** English, Spanish, French, German, and more
- **Indian:** Hindi, Bengali, Tamil, Kannada, Telugu, and more
- **East Asian:** Chinese, Japanese, Korean
- **African:** Swahili, and more

Your language choice is remembered the next time you open the dashboard.

---

## 7. Mobile & Cross-Browser Support

The dashboard is fully responsive and touch-friendly, tested across:

- **Desktop:** Chrome, Firefox, Vivaldi, Brave, Opera, Edge, Safari
- **Mobile:** Safari (iOS), Chrome (Android/iOS), Samsung Browser, Firefox (Android), Brave, Opera

Mobile-specific touches include:

- Layout reflows to a single column on phones, with larger tap targets on tabs, buttons, and inputs
- Safe-area padding so content isn't hidden behind the iPhone notch/home indicator or Android gesture bar
- Prevents iOS Safari's auto-zoom-on-input-focus behavior
- Can be added to your home screen on iOS or Android for an app-like launch icon
- Smooth momentum scrolling for the city list and hourly forecast on touch devices

---

## 8. Data Persistence

Your saved cities, their order, and your selected language are all stored in your browser's local storage. That means:

- Your list survives closing and reopening the browser or side panel
- Data is local to that specific browser on that specific device — it does not sync across browsers or devices
- Clearing your browser's site data/cache for this page will reset your saved cities and language back to defaults

---

## 9. Troubleshooting

**"City not found" alert when adding a city**
Make sure you've selected an entry from the dropdown list (rather than typing a name and pressing Enter immediately) — the dashboard needs the exact geocoded match to fetch weather data for that location.

**"Connection Failed" message on a city's panel**
This appears when the dashboard can't reach the weather data servers. Check your internet connection, or try re-adding the city — this is usually temporary.

**Dropdown suggestions not appearing on Safari (iOS)**
This is a known Safari limitation with the native suggestion list for search inputs, not a bug in the dashboard. You can still type a city name and press **Enter** or tap **Add City** to add it directly.

---

## 10. Credits & License

**Created by:** GGR, Maryland, USA
**About:** Global Time & Weather dashboard for the Vivaldi Browser Side Panel, built for the Vivaldi community.
**Inspired by:** [JRK, Sexbierum, The Netherlands](https://github.com/JRKL75/Chrono)

Copyright © 2026 GGR. You are free to use, modify, share, and redistribute this project for personal or commercial purposes. Please respect the original author by keeping this notice intact and providing appropriate credit when redistributing or publishing modified versions. This project is provided "as is," without warranty of any kind — the author accepts no liability for any damages or issues arising from its use.
