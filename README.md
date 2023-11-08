# GO client for WeatherAPI.com

# Introduction
WeatherAPI.com provides access to weather and geo data via a JSON/XML restful API. It allows developers to create desktop, web and mobile applications using this data very easy. 

We provide following data through our API:     
- Real-time weather
- 14 day weather forecast
- Historical Weather
- Marine Weather and Tide Data
- Future Weather (Upto 365 days ahead)
- Daily and hourly intervals
- 15 min interval (Enterprise only)
- Astronomy
- Time zone
- Location data
- Sports
- Search or Autocomplete API
- Weather Alerts
- Air Quality Data
- Bulk Request

# Getting Started    
You need to [signup](https://www.weatherapi.com/signup.aspx) and then you can find your API key under [your account](https://www.weatherapi.com/login.aspx), and start using API right away!  

Try our weather API by using interactive [API Explorer](https://www.weatherapi.com/api-explorer.aspx).  

We also have SDK for popular framework/languages available on [Github](https://github.com/weatherapicom/) for quick integrations.  

If you find any features missing or have any suggestions, please [contact us](https://www.weatherapi.com/contact.aspx).    

# Authentication    
API access to the data is protected by an API key. If at anytime, you find the API key has become vulnerable, please regenerate the key using Regenerate button next to the API key.    

Authentication to the WeatherAPI.com API is provided by passing your API key as request parameter through an API .      

##  key parameter  
key=YOUR API KEY

## Installation
Put the package under your project folder and add the following in import:
```golang
import "./swagger"
```

## Documentation for API Endpoints

All URIs are relative to *https://api.weatherapi.com/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*APIsApi* | [**Astronomy**](docs/APIsApi.md#astronomy) | **Get** /astronomy.json | Astronomy API
*APIsApi* | [**ForecastWeather**](docs/APIsApi.md#forecastweather) | **Get** /forecast.json | Forecast API
*APIsApi* | [**FutureWeather**](docs/APIsApi.md#futureweather) | **Get** /future.json | Future API
*APIsApi* | [**HistoryWeather**](docs/APIsApi.md#historyweather) | **Get** /history.json | History API
*APIsApi* | [**IpLookup**](docs/APIsApi.md#iplookup) | **Get** /ip.json | IP Lookup API
*APIsApi* | [**MarineWeather**](docs/APIsApi.md#marineweather) | **Get** /marine.json | Marine Weather API
*APIsApi* | [**RealtimeWeather**](docs/APIsApi.md#realtimeweather) | **Get** /current.json | Realtime API
*APIsApi* | [**SearchAutocompleteWeather**](docs/APIsApi.md#searchautocompleteweather) | **Get** /search.json | Search/Autocomplete API
*APIsApi* | [**TimeZone**](docs/APIsApi.md#timezone) | **Get** /timezone.json | Time Zone API


## Documentation For Models

 - [Alerts](docs/Alerts.md)
 - [AlertsAlert](docs/AlertsAlert.md)
 - [ArrayOfSearch](docs/ArrayOfSearch.md)
 - [Astronomy](docs/Astronomy.md)
 - [AstronomyAstro](docs/AstronomyAstro.md)
 - [Current](docs/Current.md)
 - [CurrentAirQuality](docs/CurrentAirQuality.md)
 - [CurrentCondition](docs/CurrentCondition.md)
 - [Error400](docs/Error400.md)
 - [Error401](docs/Error401.md)
 - [Error403](docs/Error403.md)
 - [Forecast](docs/Forecast.md)
 - [ForecastAstro](docs/ForecastAstro.md)
 - [ForecastCondition](docs/ForecastCondition.md)
 - [ForecastDay](docs/ForecastDay.md)
 - [ForecastDayCondition](docs/ForecastDayCondition.md)
 - [ForecastForecastday](docs/ForecastForecastday.md)
 - [ForecastHour](docs/ForecastHour.md)
 - [Ip](docs/Ip.md)
 - [Location](docs/Location.md)
 - [Marine](docs/Marine.md)
 - [MarineForecastday](docs/MarineForecastday.md)
 - [MarineHour](docs/MarineHour.md)
 - [Search](docs/Search.md)


## Documentation For Authorization

## ApiKeyAuth
- **Type**: API key 

Example
```golang
auth := context.WithValue(context.Background(), sw.ContextAPIKey, sw.APIKey{
	Key: "APIKEY",
	Prefix: "Bearer", // Omit if not necessary.
})
r, err := client.Service.Operation(auth, args)
```

## Author



