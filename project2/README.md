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
```
