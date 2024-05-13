# API Documentation for Explore California (Weather)

## Description
This API will give you a fake 5 day weather forecast for over 7000 cities around the world. You can search by city or coordinates.

## WEATHER - Base URL
http://explorecalifornia.org/api/weather/

Notes:
- You must provide parameters for the API to work. An ‘empty’ call with throw a warning.
- The results are cached by city and season therefore you will always get the same
temperature for a given city and given time of the year.

## Parameters
| Parameter name | Possible Values |
| -------------- | --------------- |
| city | Name of a city |
| lat | Search coordinate latitude value |
| lng | Search coordinate longitude value |
| radius | Radius starting from central coordinate |
| qty | Any integer value (1, 2, 3...) |
| unit | F for Fahrenheit (default) C for Celcius |

## Example Usage & Results
Get weather for a city which name contains “mia”, limiting results to 3 towns http://explorecalifornia.org/api/weather/city/mia/qty/3 or
http://explorecalifornia.org/api/weather.php?city=mia&qty=3
```
[
  {
    "id": "2015",
    "name": "Mianyang",
    "name_ascii": "Mianyang",
    "lat": "31.46997703",
    "lng": "104.7699768",
    "population": "830068",
    "country_id": "40",
    "province": "Sichuan",
    "country_name":
    "China",
    "unit": "F",
    "season": "spring",
    "forecast": [
      {
        "date": "04/14/2017",
        "temp_min": 58.442,
        "temp_max": 58.514,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "sun",
        "condition_desc": "Blue skies all day long!", "condition_video":
        "http://explorecalifornia.org/api/media/sun_45448.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/sun_16240.png"
      },
      {
        "date": "04/15/2017",
        "temp_min": 59.882,
        "temp_max": 70.952,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "storm", "condition_desc": "Watch out for storms!", "condition_video":
        "http://explorecalifornia.org/api/media/storm_190935.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/storm_16240.png"
      },
      ...
    ]
},
  {
    "id": "3774",
    "name": "Miandrivazo",
    "name_ascii": "Miandrivazo",
    "lat": "-19.51618732",
    "lng": "45.46661983",
    "population": "11894",
    "country_id": "117",
    "province": "Toliary",
    "country_name": "Madagascar",
    "unit": "F",
    "season": "fall",
    "forecast":
      ...
  },
  {
    "id": "3981",
    "name": "Miahuatlan",
    "name_ascii": "Miahuatlan",
    "lat": "16.32999676",
    "lng": "-96.60000574",
    "population": "16662",
    "country_id": "124",
    "province": "Oaxaca",
    "country_name": "Mexico",
    "unit": "F",
    "season": "spring",
    "forecast":
      ...
  },
]
```
Get weather for the city closest to the coordinates 40.0, -105.0, limiting to 1 result
http://explorecalifornia.org/api/weather/lat/40/lng/-105/qty/1
or
http://explorecalifornia.org/api/weather.php?lat=40&lng=-105&qty=1

```
[
  {
    "id": "6487",
    "name": "Boulder",
    "name_ascii": "Boulder",
    "lat": "40.03844627",
    "lng": "-105.246093",
    "population": "106898",
    "country_id": "206",
    "province": "Colorado",
    "country_name": "United States of America", "distance": "13.29067934194029",
    "unit": "F",
    "season": "winter",
    "forecast": [
      {
      "date": "03\/13\/2017",
      "temp_min": 10.81,
      "temp_max": 15.31,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "storm", "condition_desc": "Watch out for storms!", "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/storm_190935.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/storm_16240.png" },
      {
      "date": "03\/14\/2017",
      "temp_min": 12.72,
      "temp_max": 17.06,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "storm", "condition_desc": "Watch out for storms!", "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/storm_190935.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/storm_16240.png" },
      {
      "date": "03\/15\/2017",
      "temp_min": 9.03,
      "temp_max": 11.34,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "snow", "condition_desc": "It will snow!", "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/snow_1033097.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/snow_16240.png" },
      {
      "date": "03\/16\/2017",
      "temp_min": 10.02,
      "temp_max": 11.4,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "condition_desc": "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/snow_1033097.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/snow_16240.png" },
      {
      "date": "03\/17\/2017",
      "temp_min": 10.16,
      "temp_max": 18.23,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "condition_desc": "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/cloudy_4281614.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/cloudy_16240.png" },
      {
      "date": "03\/18\/2017",
      "temp_min": 8.62,
      "temp_max": 8.77,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "snow", "condition_desc": "It will snow!", "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/snow_1033097.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/snow_16240.png" },
      {
      "date": "03\/19\/2017",
      "temp_min": 10.06,
      "temp_max": 14.21,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "condition_desc": "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/cloudy_4281614.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/cloudy_16240.png" },
      {
      "date": "03\/20\/2017",
      "temp_min": 13.9,
      "temp_max": 16.59,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "condition_desc": "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/snow_1033097.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/snow_16240.png" },
      {
      "date": "03\/21\/2017",
      "temp_min": 13.96,
      "temp_max": 16.07,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "cloudy", "condition_desc": "Partially cloudy day", "condition_icon":
      "condition_video": "http:\/\/explorecalifornia.org\/api_media\/cloudy_4281614.mov",
      "condition_icon": "http:\/\/explorecalifornia.org\/api_media\/cloudy_16240.png" },
      {
      "date": "03\/22\/2017",
      "temp_min": 11.41,
      "temp_max": 17.29,
      "season_min": 8.5,
      "season_max": 20, "condition_name": "snow", "condition_desc": "It will snow!", "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/snow_1033097.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/snow_16240.png" },
      {
      "date": "03\/23\/2017",
      "temp_min": 10.71,
      "temp_max": 14.07,
      "season_min": 8.5,
      "season_max": 20,
      "condition_name": "snow", "condition_desc": "It will snow!", "condition_video":
      "http:\/\/explorecalifornia.org\/api_media\/snow_1033097.mov", "condition_icon":
      "http:\/\/explorecalifornia.org\/api_media\/snow_16240.png" }
    ]
  }
]
```

Get weather for 2 cities within 130 miles from the coordinates 40.0, -105.0
http://explorecalifornia.org/api/weather/lat/40/lng/-105/radius/130/qty/2
or
http://explorecalifornia.org/api/weather.php?lat=40&lng=-105&radius=130&qty=2

```
[
    {
      "id": "6487",
      "name": "Boulder",
      "name_ascii": "Boulder",
      "lat": "40.03844627",
      "lng": "-105.246093",
      "population": "106898",
      "country_id": "206",
      "province": "Colorado",
      "country_name": "United States of America", "distance": "13.29067934194029",
      "unit": "F",
      "season": "spring",
      "forecast": [
        {
          "date": "04/14/2017",
          "temp_min": 67.946,
          "temp_max": 74.516,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "cloudy", "condition_desc": "Partially cloudy day", "condition_video":
          "http://explorecalifornia.org/api/media/cloudy_45449.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/cloudy_16240.png" },
        {
          "date": "04/15/2017",
          "temp_min": 59.684,
          "temp_max": 77.342,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "cloudy", "condition_desc": "Partially cloudy day", "condition_video":
          "http://explorecalifornia.org/api/media/cloudy_45449.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/cloudy_16240.png" },
        {
          "date": "04/16/2017",
          "temp_min": 70.106,
          "temp_max": 71.636,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "sun",
          "condition_desc": "Blue skies all day long!", "condition_video":
          "http://explorecalifornia.org/api/media/sun_45448.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/sun_16240.png" },
        {
          "date": "04/17/2017",
          "temp_min": 59.378,
          "temp_max": 72.176,
          "season_min": 57.65,
          "season_max": 78.35, "condition_name": "rain", "condition_desc": "Wet and rainy", "condition_video":
          "http://explorecalifornia.org/api/media/rain_28580841.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/rain_16240.png" },
        {
          "date": "04/18/2017",
          "temp_min": 58.154,
          "temp_max": 62.078,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "cloudy", "condition_desc": "Partially cloudy day", "condition_video":
          "http://explorecalifornia.org/api/media/cloudy_45449.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/cloudy_16240.png" },
        {
          "date": "04/19/2017",
          "temp_min": 60.044,
          "temp_max": 65.678,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "storm", "condition_desc": "Watch out for storms!", "condition_video":
          "http://explorecalifornia.org/api/media/storm_190935.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/storm_16240.png" },
        {
          "date": "04/20/2017",
          "temp_min": 62.186,
          "temp_max": 68.216,
          "season_min": 57.65,
          "season_max": 78.35, "condition_name": "rain", "condition_desc": "Wet and rainy", "condition_video":
          "http://explorecalifornia.org/api/media/rain_28580841.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/rain_16240.png" },
        {
          "date": "04/21/2017",
          "temp_min": 64.868,
          "temp_max": 64.886,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "cloudy", "condition_desc": "Partially cloudy day", "condition_video":
          "http://explorecalifornia.org/api/media/cloudy_45449.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/cloudy_16240.png" },
        {
          "date": "04/22/2017",
          "temp_min": 63.014,
          "temp_max": 74.57,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "sun",
          "condition_desc": "Blue skies all day long!",
          "condition_video": "http://explorecalifornia.org/api/media/sun_45448.mp4",
          "condition_icon": "http://explorecalifornia.org/api/media/sun_16240.png" },
        {
          "date": "04/23/2017",
          "temp_min": 61.628,
          "temp_max": 65.264,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "sun",
          "condition_desc": "Blue skies all day long!", "condition_video":
          "http://explorecalifornia.org/api/media/sun_45448.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/sun_16240.png" },
        {
          "date": "04/24/2017",
          "temp_min": 60.962,
          "temp_max": 73.22,
          "season_min": 57.65,
          "season_max": 78.35,
          "condition_name": "rain",
          "condition_desc": "Wet and rainy",
          "condition_video":
          "http://explorecalifornia.org/api/media/rain_28580841.mp4", "condition_icon":
          "http://explorecalifornia.org/api/media/rain_16240.png"
        }
      ]
  },

  {
    "id": "6490",
    "name": "Denver",
    "name_ascii": "Denver",
    "lat": "39.73918805",
    "lng": "-104.984016",
    "population": "1930800",
    "country_id": "206",
    "province": "Colorado",
    "country_name": "United States of America",
    "distance": "18.041400842548125",
    "unit": "F",
    "season": "spring",
    "forecast": [
      {
        "date": "04/14/2017",
        "temp_min": 61.088,
        "temp_max": 75.326,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "storm", "condition_desc": "Watch out for storms!", "condition_video":
        "http://explorecalifornia.org/api/media/storm_190935.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/storm_16240.png" },
      {
        "date": "04/15/2017",
        "temp_min": 63.104,
        "temp_max": 67.172,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "cloudy", "condition_desc": "Partially cloudy day", "condition_video":
        "http://explorecalifornia.org/api/media/cloudy_45449.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/cloudy_16240.png" },
      {
        "date": "04/16/2017",
        "temp_min": 59.126,
        "temp_max": 61.304,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "sun",
        "condition_desc": "Blue skies all day long!", "condition_video":
        "http://explorecalifornia.org/api/media/sun_45448.mp4",
        "condition_icon": "http://explorecalifornia.org/api/media/sun_16240.png" },
      {
        "date": "04/17/2017",
        "temp_min": 71.834,
        "temp_max": 77.864,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "cloudy", "condition_desc": "Partially cloudy day", "condition_video":
        "http://explorecalifornia.org/api/media/cloudy_45449.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/cloudy_16240.png" },
      {
        "date": "04/18/2017",
        "temp_min": 66.524,
        "temp_max": 66.812,
        "season_min": 57.65,
        "season_max": 78.35, "condition_name": "rain", "condition_desc": "Wet and rainy", "condition_video":
        "http://explorecalifornia.org/api/media/rain_28580841.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/rain_16240.png" },
      {
        "date": "04/19/2017",
        "temp_min": 57.884,
        "temp_max": 58.874,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "sun",
        "condition_desc": "Blue skies all day long!", "condition_video":
        "http://explorecalifornia.org/api/media/sun_45448.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/sun_16240.png" },
      {
        "date": "04/20/2017",
        "temp_min": 67.676,
        "temp_max": 77.36,
        "season_min": 57.65,
        "season_max": 78.35, "condition_name": "rain", "condition_desc": "Wet and rainy", "condition_video":
        "http://explorecalifornia.org/api/media/rain_28580841.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/rain_16240.png" },
      {
        "date": "04/21/2017",
        "temp_min": 63.716,
        "temp_max": 64.148,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "cloudy", "condition_desc": "Partially cloudy day", "condition_video":
        "http://explorecalifornia.org/api/media/cloudy_45449.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/cloudy_16240.png" },
      {
        "date": "04/22/2017",
        "temp_min": 59.702,
        "temp_max": 70.448,
        "season_min": 57.65,
        "season_max": 78.35, "condition_name": "rain", "condition_desc": "Wet and rainy", "condition_video":
        "http://explorecalifornia.org/api/media/rain_28580841.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/rain_16240.png" },
      {
        "date": "04/23/2017",
        "temp_min": 57.704,
        "temp_max": 58.64,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "sun",
        "condition_desc": "Blue skies all day long!", "condition_video":
        "http://explorecalifornia.org/api/media/sun_45448.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/sun_16240.png" },
      {
        "date": "04/24/2017",
        "temp_min": 59.324,
        "temp_max": 61.88,
        "season_min": 57.65,
        "season_max": 78.35,
        "condition_name": "storm", "condition_desc": "Watch out for storms!", "condition_video":
        "http://explorecalifornia.org/api/media/storm_190935.mp4", "condition_icon":
        "http://explorecalifornia.org/api/media/storm_16240.png" }
    ]
  }
]
```
