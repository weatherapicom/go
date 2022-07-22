# Go API client for WeatherAPI.com

# Introduction  
WeatherAPI.com provides access to weather and geo data via a JSON/XML restful API. It allows developers to create desktop, web and mobile applications using this data very easy.    

We provide following data through our API:     
- Real-time weather 
- 14 day weather forecast 
- Astronomy 
- Time zone 
- Location data 
- Search or Autocomplete API 
- NEW: Historical weather 
- NEW: Future Weather (Upto 300 days ahead) 
- Weather Alerts 
- Air Quality Data  

# Getting Started    
You need to [signup](https://www.weatherapi.com/signup.aspx) and then you can find your API key under [your account](https://www.weatherapi.com/login.aspx), and start using API right away!    

We have [code libraries](https://www.weatherapi.com/docs/code-libraries.aspx) for different programming languages like PHP, .net, JAVA, etc.  If you find any features missing or have any suggestions, please [contact us](https://www.weatherapi.com/contact.aspx).    

# Authentication    
API access to the data is protected by an API key. If at anytime, you find the API key has become vulnerable, please regenerate the key using Regenerate button next to the API key.  Authentication to the WeatherAPI.com API is provided by passing your API key as request parameter through an API .      

##  key parameter  
key=<YOUR API KEY>  

## Overview
This API client was generated by the [swagger-codegen](https://github.com/swagger-api/swagger-codegen) project.  By using the [swagger-spec](https://github.com/swagger-api/swagger-spec) from a remote server, you can easily generate an API client.

- API version: 1.0.0-oas3
- Package version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.go.GoClientCodegen

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
*APIsApi* | [**RealtimeWeather**](docs/APIsApi.md#realtimeweather) | **Get** /current.json | Realtime API
*APIsApi* | [**SearchAutocompleteWeather**](docs/APIsApi.md#searchautocompleteweather) | **Get** /search.json | Search/Autocomplete API
*APIsApi* | [**TimeZone**](docs/APIsApi.md#timezone) | **Get** /timezone.json | Time Zone API

## Documentation For Models

 - [Alerts](docs/Alerts.md)
 - [AlertsAlert](docs/AlertsAlert.md)
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
 - [InlineResponse200](docs/InlineResponse200.md)
 - [InlineResponse2001](docs/InlineResponse2001.md)
 - [InlineResponse2002](docs/InlineResponse2002.md)
 - [InlineResponse2003](docs/InlineResponse2003.md)
 - [Ip](docs/Ip.md)
 - [Location](docs/Location.md)
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


