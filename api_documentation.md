# Prayer Times & Lunar Observation Calculator API Documentation
# By Mr. Ahmed RASNAAMA

This document describes the HTTP API endpoints provided by the Prayer Times Calculator server. The server runs on port `8080` by default.

All endpoints support both **GET** (using query parameters) and **POST** (using a JSON body). 

---

## 1. Single-Day Prayer Times API

Calculates high-accuracy astronomical prayer times for a specific location and date.

* **Endpoints:** 
  * `GET /api/times`
  * `POST /api/times`
* **Content-Type:** `application/json` (for POST request)

### Request Parameters

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `lat` | Float | Yes | Latitude of the location (between `-90.0` and `90.0` degrees). |
| `lng` | Float | Yes | Longitude of the location (between `-180.0` and `180.0` degrees). |
| `elv` | Float | No | Elevation above sea level in meters. (Default: `0.0`). |
| `tz` | Float | No | Timezone offset in hours from UTC. (Default: `0.0`). |
| `date` | String | No | Date in `YYYY-MM-DD` format. (Default: current date). |
| `method` | String | No | Preset calculation method. Options: `MWL`, `ISNA`, `Egypt`, `UmmAlQura`, `Gulf`, `Karachi`, `Tehran`, `Jafari`, `Kuwait`, `UOIF`, `Kemenag`, `MUIS`, `JAKIM`, `Moonsighting`. |
| `asr` | String | No | Fiqh school for Asr prayer. Options: `Standard` (Shafi'i, Maliki, Hanbali), `Hanafi`. |
| `high_lats` | String | No | High-latitude adjustment method. Options: `NightMiddle`, `OneSeventh`, `AngleBased`, `None`. |
| `shafaq` | String | No | Shafaq setting (only if method is `Moonsighting`). Options: `General`, `Abyad`, `Ahmer`. |

### Example Request (POST)

* **URL:** `http://localhost:8080/api/times`
* **Body:**
```json
{
  "lat": 21.42252,
  "lng": 39.82621,
  "elv": 277.0,
  "tz": 3.0,
  "date": "2026-05-18",
  "method": "UmmAlQura"
}
```

### Example Response

```json
{
  "date": "2026-05-18",
  "location": {
    "latitude": 21.42252,
    "longitude": 39.82621,
    "elevation": 277.0,
    "timezone": 3.0
  },
  "settings": {
    "method": "UmmAlQura",
    "sun_calc_method": "USNO",
    "asr_school": "Standard",
    "high_latitude_adjustment": "NightMiddle",
    "moonsighting_shafaq": "General"
  },
  "times": {
    "imsak": "04:00:54",
    "fajr": "04:10:54",
    "sunrise": "05:37:12",
    "dhuhr": "12:18:24",
    "asr": "15:35:48",
    "sunset": "18:59:36",
    "maghrib": "18:59:36",
    "isha": "20:29:36",
    "midnight": "23:48:24"
  }
}
```

---

## 2. Date Range Prayer Times API

Calculates prayer times for a range of dates (up to 366 days).

* **Endpoints:**
  * `GET /api/times/range`
  * `POST /api/times/range`

### Request Parameters

In addition to the parameters for a single day, this API requires:

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `start_date` | String | Yes | Start date in `YYYY-MM-DD` format. |
| `end_date` | String | Yes | End date in `YYYY-MM-DD` format. |

### Example Request (POST)

* **URL:** `http://localhost:8080/api/times/range`
* **Body:**
```json
{
  "lat": 21.42252,
  "lng": 39.82621,
  "start_date": "2026-05-18",
  "end_date": "2026-05-19"
}
```

---

## 3. Lunar Observation API

Predicts the new moon crescent visibility and the start of the Hijri month for a given range of dates.

* **Endpoints:**
  * `GET /api/lunar`
  * `POST /api/lunar`

### Request Parameters

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `lat` | Float | Yes | Latitude of the location. |
| `lng` | Float | Yes | Longitude of the location. |
| `elv` | Float | No | Elevation above sea level in meters. |
| `tz` | Float | No | Timezone offset in hours from UTC. |
| `start_date` | String | Yes | Start date in `YYYY-MM-DD` format. |
| `end_date` | String | Yes | End date in `YYYY-MM-DD` format. |
| `temp` | Float | No | Ambient temperature in Celsius. (Default: `10.0`). |
| `pressure` | Float | No | Atmospheric pressure in mbar. (Default: `1010.0`). |

### Example Request (POST)

* **URL:** `http://localhost:8080/api/lunar`
* **Body:**
```json
{
  "lat": 21.42252,
  "lng": 39.82621,
  "elv": 277.0,
  "tz": 3.0,
  "start_date": "2026-05-17",
  "end_date": "2026-05-18"
}
```

### Example Response (Truncated)

```json
[
  {
    "date": "2026-05-17",
    "jd_sunset": 2453872.16,
    "conjunction_time": "2026-05-16 20:09:12 UT",
    "moon_age_at_sunset": 19.68,
    "sunset_time": "18:50:12",
    "moonset_time": "19:24:12",
    "lag_time": 34.0,
    "best_time": "19:05:18",
    "moon_altitude": 4.25,
    "moon_azimuth": 284.12,
    "sun_altitude": -5.12,
    "sun_azimuth": 286.32,
    "arc_of_vision": 9.37,
    "relative_azimuth": 2.20,
    "elongation": 9.62,
    "crescent_width": 0.12,
    "yallop_q": -0.25,
    "yallop_category": "E",
    "yallop_description": "Not visible with standard telescope",
    "odeh_v": -1.25,
    "odeh_category": "D",
    "odeh_description": "Not visible",
    "is_hijri_start": false,
    "is_umm_al_qura_start": false
  },
  {
    "date": "2026-05-18",
    "jd_sunset": 2453873.16,
    "conjunction_time": "2026-05-16 20:09:12 UT",
    "moon_age_at_sunset": 43.68,
    "sunset_time": "18:50:48",
    "moonset_time": "20:05:48",
    "lag_time": 75.0,
    "best_time": "19:24:08",
    "moon_altitude": 12.18,
    "moon_azimuth": 279.42,
    "sun_altitude": -8.84,
    "sun_azimuth": 285.84,
    "arc_of_vision": 21.02,
    "relative_azimuth": 6.42,
    "elongation": 21.98,
    "crescent_width": 0.58,
    "yallop_q": 0.85,
    "yallop_category": "A",
    "yallop_description": "Easily visible to the naked eye",
    "odeh_v": 8.42,
    "odeh_category": "A",
    "odeh_description": "Visible with the naked eye",
    "is_hijri_start": false,
    "is_umm_al_qura_start": true
  }
]
```

---

## 4. Global Visibility Map API

Generates a packed global grid representing crescent visibility categories for mapping engines (like Leaflet).

* **Endpoints:**
  * `GET /api/lunar/map`
  * `POST /api/lunar/map`

### Request Parameters

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `date` | String | Yes | target observation date in `YYYY-MM-DD` format. |
| `step` | Float | No | Step resolution in degrees. Range: `2.0` (fine) to `10.0` (coarse). (Default: `3.0`). |
| `temp` | Float | No | Atmospheric temperature in Celsius. |
| `pressure` | Float | No | Atmospheric pressure in mbar. |
| `elv` | Float | No | Observer elevation in meters. |

### Example Request (POST)

* **URL:** `http://localhost:8080/api/lunar/map`
* **Body:**
```json
{
  "date": "2026-05-18",
  "step": 3.0
}
```

### Example Response

```json
{
  "date": "2026-05-18",
  "lat_min": -75.0,
  "lat_max": 75.0,
  "lat_step": 3.0,
  "lng_min": -180.0,
  "lng_max": 180.0,
  "lng_step": 3.0,
  "grid": [
    80, 80, 80, 0, 0, 85, 85
  ]
}
```

*Note: The `grid` elements are packed 1-byte values containing the category codes. The lower 4 bits represent the Yallop category code (`0` to `5`), and the upper 4 bits represent the Odeh category code (`0` to `5`).*
