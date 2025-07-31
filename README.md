# USGS Earthquake Visualization Auto-Updater

**Interactive, real-time earthquake dashboard for global monitoring—powered by the USGS Earthquake API. User-selectable time window, live fault lines, magnitude-coded markers, and full table view. 100% browser-based.**

---

## \:globe\_with\_meridians: Overview

This web application provides a real-time, interactive visualization of global earthquake activity, using authoritative live data from the [USGS (United States Geological Survey) Earthquake API](https://earthquake.usgs.gov/fdsnws/event/1/). Designed for both researchers and the general public, the app is suitable for education, industry, and rapid situational awareness.

---

## \:star2: Features

* **Live Earthquake Data:**
  Automatically fetches and displays recent earthquake events from the USGS API.
  Includes magnitude, precise location, depth, UTC timestamp, and a direct USGS event link.

* **User-Selectable Time Window:**
  Choose to view earthquakes from the last 5 min, 10 min, 15 min, 30 min, 1 hour, 1 day, 7 days, up to 1 year.
  The dropdown instantly updates the map and table, so you can analyze trends at any scale.

* **Auto-Updating Visualization:**
  The dashboard automatically refreshes every 5 minutes, ensuring data is always current.
  No need to reload your browser manually.

* **Rich Interactive Map:**

  * **Markers clustered** for clarity; color-coded by Richter scale.
  * **Animated/blinking** marker for earthquakes in the last 5 minutes (real-time monitoring).
  * **Popup for each marker**: Magnitude, location, depth, time, and USGS reference.
  * **Fault lines overlay:** Tectonic plate boundaries are shown in purple for scientific context.

* **Dynamic Table Panel:**

  * Scrollable table lists all events in the current window, most recent at the top.
  * Columns: Magnitude, location (with details), time, and depth.
  * Magnitudes are color-coded for instant risk assessment.

* **Mobile Friendly & Responsive:**

  * Layout adapts for mobile and tablets.
  * No installation required—just open the HTML file.

* **No Backend or Server Needed:**
  All computation and rendering happens in the browser. No dependencies other than a modern browser and Internet connection.

---

## \:rocket: Quick Start

**1. Download or clone this repository.**

```bash
git clone https://github.com/yourusername/usgs-earthquake-visualization.git
cd usgs-earthquake-visualization
```

**2. Open `index.html` in your web browser.**
*No build step required!*

**3. Select your preferred time window from the dropdown.**
*The map and table update instantly, and will auto-refresh every 5 minutes.*

---

## \:mag: How It Works

* **Data Source:**
  Live data is retrieved from the [USGS FDSN Event Web Service](https://earthquake.usgs.gov/fdsnws/event/1/), using a browser-based [Axios](https://axios-http.com/) request.

* **Map Engine:**
  Uses [Leaflet.js](https://leafletjs.com/) and [Leaflet.markercluster](https://github.com/Leaflet/Leaflet.markercluster) for robust, scalable mapping.

* **Fault Lines:**
  Tectonic boundaries are overlaid using the [PB2002 plate boundary dataset](https://github.com/fraxen/tectonicplates).

* **Color Coding:**
  Magnitude bins (Richter scale) are visually mapped to marker colors:

  * Micro (0–2): Blue
  * Minor (2–3): Green
  * Light (3–4): Yellow
  * Moderate (4–5): Light Orange
  * Strong (5–6): Orange
  * Major (6–7): Red
  * Great (7+): Dark Red

* **Auto-Update:**
  A `setInterval` in JavaScript re-queries the API every 5 minutes, refreshing both map and table in-place.

---

## \:hammer\_and\_wrench: Dependencies

All dependencies are loaded via CDN, so you do **not** need to install anything.

* [Leaflet.js](https://leafletjs.com/)
* [Leaflet.markercluster](https://github.com/Leaflet/Leaflet.markercluster)
* [Axios](https://axios-http.com/)
* [USGS Earthquake API](https://earthquake.usgs.gov/fdsnws/event/1/)
* [PB2002 Fault Lines GeoJSON](https://github.com/fraxen/tectonicplates)

---

## \:bulb: Usage Tips

* **Browser Support:**
  Works best in latest Chrome, Firefox, Edge, Safari.

* **Map Controls:**

  * Click any marker for full details and USGS event link.
  * Zoom and pan the map to focus on any region.

* **API Limitations:**

  * USGS API allows up to 20,000 events per query; querying long periods (months/years) may not show every small quake.
  * The "Last 1 year" option may skip some minor events.

* **Customization:**

  * You can easily change the auto-update interval (default 5 min = 300000 ms).
  * Add/remove time window options by editing the `<select>` block in the HTML.

---

## \:warning: Troubleshooting

* **Map is blank:**
  Ensure you are online; the map and data are loaded live from the internet.

* **No data for short window:**
  Selecting a very short window (like 5 min) may show zero events if no earthquakes occurred.

* **API errors:**
  Occasionally, the USGS API may throttle requests or have temporary outages.

* **Mobile glitches:**
  For best results on mobile, view in landscape orientation.

---

## \:triangular\_ruler: Extensibility

* **Add new map layers** (e.g., aftershocks, tsunami zones) by modifying the JavaScript.
* **Integrate with other hazard APIs** (e.g., volcanoes, floods) for multi-risk dashboards.
* **Fork and build your own custom earthquake analytics platform!**

---

## \:handshake: Credits

Developed by [Partha Pratim Ray](mailto:parthapratimray1986@gmail.com), July 2025, India.
Powered by USGS Earthquake Data and open-source geospatial tools.

---

## \:scroll: License

### MIT License

```
MIT License

Copyright (c) 2025 Partha Pratim Ray

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## \:envelope: Contact & Contributions

* Questions, suggestions, or issues?
  Email [parthapratimray1986@gmail.com](mailto:parthapratimray1986@gmail.com) or open an issue/pull request on GitHub.
* Contributions, forks, and scientific use are warmly welcomed.

---

**Explore live earthquake data and help build a more resilient world!** 🌏

---

