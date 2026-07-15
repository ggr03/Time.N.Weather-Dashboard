# Time.N.Weather -- Dashboard
Global Time and Weather dashboard that allows users to track live local times, current weather conditions, and multi-day forecasts for major cities worldwide. Created for the Vivaldi Browser side Panel and Vivaldi Community.

Inspired by the work done by [JRK, Sexbierum, The Netherlands.](https://github.com/JRKL75/Chrono) - [Vivaldi Forum](https://forum.vivaldi.net/topic/119442/chrono-add-multiple-timezones-in-sidepanel-1-file-no-dependencies)

This guide covers everything you need to know to navigate the interface, manage your locations, and understand the deep meteorological and astronomical data provided in the bento-grid layouts.

---

## 1. Managing Your Cities

The dashboard allows you to track multiple locations worldwide, complete with their local timezones and localized weather data.

### Adding a New City

The dashboard uses a live, high-precision geocoding API to find exact global locations.

1. Locate the **Search Bar** at the top left of the sidebar.
2. Begin typing the name of a city (you must type at least 2 characters).
3. **Wait a brief moment.** A dropdown list will automatically populate with matches from the global database, showing the city, region/state, and country to help you differentiate between places with the same name (e.g., *London, England* vs. *London, Ontario*).
4. Select the correct city from the dropdown list.
5. Click the **"Add City"** button (or press `Enter` on your keyboard). The city will appear as a new tab in your sidebar.
<img width="511" height="501" alt="20260714_205740_Screentshot" src="https://github.com/user-attachments/assets/6d00c639-88de-415c-9b08-24450cedb3a0" />

### Rearranging Cities

You can customize the order of your saved cities using the native Drag-and-Drop feature.

1. **Hover** over any city tab you want to move. Your cursor will change to a "grab" hand.
2. **Click and hold** the tab. The tab will become slightly transparent to indicate it is being dragged.
3. **Drag** the tab up or down the list. As you hover over other tabs, a dashed blue border will appear, indicating exactly where the tab will land.
4. **Release** the mouse button to drop the tab into its new position. Your new custom order is saved automatically.

*(Note: When you click a tab to view its weather, it will "pop up" with a 3D shadow effect to indicate it is the active view. Unselected tabs remain flat.)*

---

## 2. Reading Local Weather Information

When you select the **Local Weather** tab in the main view, you are presented with a "bento-box" grid of current meteorological conditions. Here is how to read each card:

* **Condition & Temp:** Displays the current weather icon (e.g., ⛅ Partly Cloudy), the actual air temperature in both Celsius and Fahrenheit, and the "Feels like" (apparent) temperature, which factors in humidity and wind chill.
* **Sunrise & Sunset:** The exact local times the sun will crest the horizon in the morning (🌅) and disappear in the evening (🌇).
* **Moonrise & Moonset:** The exact local times the moon will appear (🌛) and set (🌜) for that specific city.
* **Solar Position:** Tracks the sun's exact physical location in the sky relative to the city:
* *Noon / Nadir:* The time the sun reaches its highest point (Solar Noon) and lowest point beneath the earth (Nadir).
* *Azimuth:* The compass direction of the sun (in degrees).
* *Altitude:* The height of the sun above the horizon (in degrees).


* **Day & Night Length:** The total duration of daylight (☀️) versus the total duration of nighttime darkness (🌙) for the current 24-hour cycle.
* **Air Quality (AQI):** The current US Air Quality Index score. The number and text will change colors (Green, Yellow, Orange, Red, Purple) to indicate health risks, ranging from "Good" to "Hazardous."
* **Humidity:** The amount of water vapor in the air as a percentage, paired with the **Dewpoint** (the temperature at which dew forms, indicating how "muggy" the air feels).
* **Wind Speed:** The current sustained wind speed measured in miles per hour (mph).
* **Air Pressure:** The atmospheric surface pressure measured in hectopascals (hPa).
* **Max UV Index:** The predicted peak ultraviolet radiation level for the day, helping you gauge sun exposure risk.
<img width="1516" height="1006" alt="Time   Weather--2026--2026-07-14 20 58 33" src="https://github.com/user-attachments/assets/7c4870a7-10de-4e94-a1ad-e745a7a4561b" />

---

## 3. Reading Lunar Metrics & Lighting Stats

By clicking the **Lunar Metrics** toggle, the dashboard swaps to advanced astronomical data calculated using the exact latitude and longitude of your selected city.

### The Lunar Bento Cards

* **Moon Phase:** Displays a visual icon and the astronomical name of the current phase (e.g., *Waxing Crescent*, *Waning Gibbous*).
* **Illumination:** The exact percentage of the moon's surface currently lit by the sun and visible from Earth.
* **Earth Distance:** The real-time geocentric distance between the Earth and the Moon, measured in kilometers.
* **Next Full Moon / Next New Moon:** The exact upcoming calendar dates when the moon will reach 100% illumination (Full) and 0% illumination (New).
* **Moon Age:** The number of days that have passed since the last New Moon, tracking progress through the ~29.5-day synodic cycle.

### The Lighting Grid (Photography & Civil Data)

Below the Lunar cards are the Morning and Evening Lighting panels. These track specific angles of the sun beneath the horizon, which dictate light quality for photography and civil twilight phases:

* **Blue Hour:** The period when the sun is between -8° and -4° below the horizon. The sky takes on a deep blue hue, ideal for landscape and city photography.
* **Golden Hour:** The period when the sun is between -4° below and +6° above the horizon. The light is soft, warm, and highly sought after by photographers.
* **Twilights:**
* *Astronomical Twilight:* The darkest phase. The sun is -18° to -12° below the horizon. Stars are fully visible, but the horizon is barely distinguishable.
* *Nautical Twilight:* The sun is -12° to -6° below the horizon. The horizon is visible, and sailors can navigate via stars.
* *Civil Twilight:* The brightest twilight. The sun is -6° to 0° below the horizon. There is enough natural light to perform outdoor activities without artificial lighting.
<img width="1474" height="993" alt="Time   Weather--2026--2026-07-14 21 00 06" src="https://github.com/user-attachments/assets/f9c45809-d90c-4985-af15-95b44072140f" />
