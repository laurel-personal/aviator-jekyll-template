---
title: /weatherdata
position: 1.6
type: get
description: Hi -- testing that the new stuff gets in. Gets the full weather data details, including temperature, wind, astronomy, and more.
right_code: |
  ~~~ json
  return: |
    [
    {
    "query": {
    "count": 1,
    "created": "2014-05-03T03:57:53Z",
    "lang": "en-US",
    "results": {
      "channel": {
        "title": "Yahoo! Weather - Tebrau, MY",
        "link": "http://us.rd.yahoo.com/dailynews/rss/weather/Tebrau__MY/*http://weather.yahoo.com/forecast/MYXX0004_c.html",
        "description": "Yahoo! Weather for Tebrau, MY",
        "language": "en-us",
        "lastBuildDate": "Sat, 03 May 2014 11:00 am MYT",
        "ttl": "60",
        "location": {
          "city": "Tebrau",
          "country": "Malaysia",
          "region": ""
        },
        "units": {
          "distance": "km",
          "pressure": "mb",
          "speed": "km/h",
          "temperature": "C"
        },
        "wind": {
          "chill": "32",
          "direction": "170",
          "speed": "4.83"
        },
        "atmosphere": {
          "humidity": "66",
          "pressure": "982.05",
          "rising": "0",
          "visibility": "9.99"
        },
        "astronomy": {
          "sunrise": "6:57 am",
          "sunset": "7:06 pm"
        },
        "image": {
          "title": "Yahoo! Weather",
          "width": "142",
          "height": "18",
          "link": "http://weather.yahoo.com",
          "url": "http://l.yimg.com/a/i/brand/purplelogo//uh/us/news-wea.gif"
        },
        "item": {
          "title": "Conditions for Tebrau, MY at 11:00 am MYT",
          "lat": "1.58",
          "long": "103.74",
          "link": "http://us.rd.yahoo.com/dailynews/rss/weather/Tebrau__MY/*http://weather.yahoo.com/forecast/MYXX0004_c.html",
          "pubDate": "Sat, 03 May 2014 11:00 am MYT",
          "condition": {
            "code": "28",
            "date": "Sat, 03 May 2014 11:00 am MYT",
            "temp": "32",
            "text": "Mostly Cloudy"
          },
          "description": "\n<img src=\"http://l.yimg.com/a/i/us/we/52/28.gif\"/><br />\n<b>Current Conditions:</b><br />\nMostly Cloudy, 32 C<BR />\n<BR /><b>Forecast:</b><BR />\nSat - Scattered Thunderstorms. High: 32 Low: 26<br />\nSun - Thunderstorms. High: 33 Low: 27<br />\nMon - Scattered Thunderstorms. High: 32 Low: 26<br />\nTue - Thunderstorms. High: 32 Low: 26<br />\nWed - Scattered Thunderstorms. High: 32 Low: 27<br />\n<br />\n<a href=\"http://us.rd.yahoo.com/dailynews/rss/weather/Tebrau__MY/*http://weather.yahoo.com/forecast/MYXX0004_c.html\">Full Forecast at Yahoo! Weather</a><BR/><BR/>\n(provided by <a href=\"http://www.weather.com\" >The Weather Channel</a>)<br/>\n",
          "forecast": [
            {
              "code": "38",
              "date": "3 May 2014",
              "day": "Sat",
              "high": "32",
              "low": "26",
              "text": "Scattered Thunderstorms"
            },
            {
              "code": "4",
              "date": "4 May 2014",
              "day": "Sun",
              "high": "33",
              "low": "27",
              "text": "Thunderstorms"
            },
            {
              "code": "38",
              "date": "5 May 2014",
              "day": "Mon",
              "high": "32",
              "low": "26",
              "text": "Scattered Thunderstorms"
            },
            {
              "code": "4",
              "date": "6 May 2014",
              "day": "Tue",
              "high": "32",
              "low": "26",
              "text": "Thunderstorms"
            },
            {
              "code": "38",
              "date": "7 May 2014",
              "day": "Wed",
              "high": "32",
              "low": "27",
              "text": "Scattered Thunderstorms"
            }
          ],
          "guid": {
            "isPermaLink": "false",
            "content": "MYXX0004_2014_05_07_7_00_MYT"
          }
        }
      }
    }
    }
    }
    ]
  ~~~
  {: title="Response" }

  ~~~ json
  {
    "error": true,
    "message": "Not supported."
  }
  ~~~
  {: title="Error" }
---
lat
: The latitude for the weather location. For example, `37.3708698`.

lng
: The longitude for the weather location. for example, `-122.037593`.

These values will be added as query parameters.
{: .success }

The following code sample shows how to make a request using jQuery AJAX:

~~~ javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "dataType": "json",
  "url": "https://simple-weather.p.mashape.com/weatherdata?lat=37.3708698&lng=-122.037593",
  "method": "GET",
  "headers": {
    "x-mashape-key": "EF3g83pKnzmshgoksF83V6JB6QyTp1cGrrdjsnczTkkYgYrp8p",
    "accept": "application/json",
    "cache-control": "no-cache",
    "postman-token": "f8b3c945-f615-ed8d-e15c-aef95acc7fa7"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
~~~
{: title="jQuery" }
