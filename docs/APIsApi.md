# \APIsApi

All URIs are relative to *https://api.weatherapi.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Astronomy**](APIsApi.md#Astronomy) | **Get** /astronomy.json | Astronomy API
[**ForecastWeather**](APIsApi.md#ForecastWeather) | **Get** /forecast.json | Forecast API
[**FutureWeather**](APIsApi.md#FutureWeather) | **Get** /future.json | Future API
[**HistoryWeather**](APIsApi.md#HistoryWeather) | **Get** /history.json | History API
[**IpLookup**](APIsApi.md#IpLookup) | **Get** /ip.json | IP Lookup API
[**MarineWeather**](APIsApi.md#MarineWeather) | **Get** /marine.json | Marine Weather API
[**RealtimeWeather**](APIsApi.md#RealtimeWeather) | **Get** /current.json | Realtime API
[**SearchAutocompleteWeather**](APIsApi.md#SearchAutocompleteWeather) | **Get** /search.json | Search/Autocomplete API
[**TimeZone**](APIsApi.md#TimeZone) | **Get** /timezone.json | Time Zone API


# **Astronomy**
> interface{} Astronomy(ctx, q, dt)
Astronomy API

Return Location and Astronomy Object

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 
  **dt** | **string**| Date on or after 1st Jan, 2015 in yyyy-MM-dd format | 

### Return type

**interface{}**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ForecastWeather**
> interface{} ForecastWeather(ctx, q, days, optional)
Forecast API

Forecast weather API method returns, depending upon your price plan level, upto next 14 day weather forecast and weather alert as json or xml. The data is returned as a Forecast Object.<br /><br />Forecast object contains astronomy data, day weather forecast and hourly interval weather information for a given city.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 
  **days** | **int32**| Number of days of weather forecast. Value ranges from 1 to 14 | 
 **optional** | ***APIsApiForecastWeatherOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a APIsApiForecastWeatherOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **dt** | **optional.String**| Date should be between today and next 14 day in yyyy-MM-dd format. e.g. &#39;2015-01-01&#39; | 
 **unixdt** | **optional.Int32**| Please either pass &#39;dt&#39; or &#39;unixdt&#39; and not both in same request. unixdt should be between today and next 14 day in Unix format. e.g. 1490227200 | 
 **hour** | **optional.Int32**| Must be in 24 hour. For example 5 pm should be hour&#x3D;17, 6 am as hour&#x3D;6 | 
 **lang** | **optional.String**| Returns &#39;condition:text&#39; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#39;lang-code&#39;. | 
 **alerts** | **optional.String**| Enable/Disable alerts in forecast API output. Example, alerts&#x3D;yes or alerts&#x3D;no. | 
 **aqi** | **optional.String**| Enable/Disable Air Quality data in forecast API output. Example, aqi&#x3D;yes or aqi&#x3D;no. | 
 **tp** | **optional.Int32**| Get 15 min interval or 24 hour average data for Forecast and History API. Available for Enterprise clients only. E.g:- tp&#x3D;15 | 

### Return type

**interface{}**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FutureWeather**
> interface{} FutureWeather(ctx, q, optional)
Future API

Future weather API method returns weather in a 3 hourly interval in future for a date between 14 days and 365 days from today in the future.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 
 **optional** | ***APIsApiFutureWeatherOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a APIsApiFutureWeatherOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dt** | **optional.String**| Date should be between 14 days and 300 days from today in the future in yyyy-MM-dd format (i.e. dt&#x3D;2023-01-01) | 
 **lang** | **optional.String**| Returns &#39;condition:text&#39; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#39;lang-code&#39;. | 

### Return type

**interface{}**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **HistoryWeather**
> interface{} HistoryWeather(ctx, q, dt, optional)
History API

History weather API method returns historical weather for a date on or after 1st Jan, 2010 as json. The data is returned as a Forecast Object.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 
  **dt** | **string**| Date on or after 1st Jan, 2015 in yyyy-MM-dd format | 
 **optional** | ***APIsApiHistoryWeatherOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a APIsApiHistoryWeatherOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **unixdt** | **optional.Int32**| Please either pass &#39;dt&#39; or &#39;unixdt&#39; and not both in same request.&lt;br /&gt;unixdt should be on or after 1st Jan, 2015 in Unix format | 
 **endDt** | **optional.String**| Date on or after 1st Jan, 2015 in yyyy-MM-dd format&lt;br /&gt;&#39;end_dt&#39; should be greater than &#39;dt&#39; parameter and difference should not be more than 30 days between the two dates. | 
 **unixendDt** | **optional.Int32**| Date on or after 1st Jan, 2015 in Unix Timestamp format&lt;br /&gt;unixend_dt has same restriction as &#39;end_dt&#39; parameter. Please either pass &#39;end_dt&#39; or &#39;unixend_dt&#39; and not both in same request. e.g. unixend_dt&#x3D;1490227200 | 
 **hour** | **optional.Int32**| Must be in 24 hour. For example 5 pm should be hour&#x3D;17, 6 am as hour&#x3D;6 | 
 **lang** | **optional.String**| Returns &#39;condition:text&#39; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#39;lang-code&#39;. | 

### Return type

**interface{}**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **IpLookup**
> Ip IpLookup(ctx, q)
IP Lookup API

IP Lookup API method allows a user to get up to date information for an IP address.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass IP address. | 

### Return type

[**Ip**](ip.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MarineWeather**
> interface{} MarineWeather(ctx, q, days, optional)
Marine Weather API

Marine weather API method returns upto next 7 day (depending upon your price plan level) marine and sailing weather forecast and tide data (depending upon your price plan level) as json or xml. The data is returned as a Marine Object.<br /><br />Marine object, depending upon your price plan level, contains astronomy data, day weather forecast and hourly interval weather information and tide data for a given sea/ocean point.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass Latitude/Longitude (decimal degree) which is on a sea/ocean. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 
  **days** | **int32**| Number of days of weather forecast. Value ranges from 1 to 7 | 
 **optional** | ***APIsApiMarineWeatherOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a APIsApiMarineWeatherOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **dt** | **optional.String**| Date should be between today and next 7 day in yyyy-MM-dd format. e.g. &#39;2023-05-20&#39; | 
 **unixdt** | **optional.Int32**| Please either pass &#39;dt&#39; or &#39;unixdt&#39; and not both in same request. unixdt should be between today and next 7 day in Unix format. e.g. 1490227200 | 
 **hour** | **optional.Int32**| Must be in 24 hour. For example 5 pm should be hour&#x3D;17, 6 am as hour&#x3D;6 | 
 **lang** | **optional.String**| Returns &#39;condition:text&#39; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#39;lang-code&#39;. | 

### Return type

**interface{}**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **RealtimeWeather**
> interface{} RealtimeWeather(ctx, q, optional)
Realtime API

Current weather or realtime weather API method allows a user to get up to date current weather information in json and xml. The data is returned as a Current Object.<br /><br />Current object contains current or realtime weather information for a given city.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 
 **optional** | ***APIsApiRealtimeWeatherOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a APIsApiRealtimeWeatherOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **lang** | **optional.String**| Returns &#39;condition:text&#39; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#39;lang-code&#39;. | 

### Return type

**interface{}**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **SearchAutocompleteWeather**
> ArrayOfSearch SearchAutocompleteWeather(ctx, q)
Search/Autocomplete API

WeatherAPI.com Search or Autocomplete API returns matching cities and towns as an array of Location object.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 

### Return type

[**ArrayOfSearch**](ArrayOfSearch.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **TimeZone**
> Location TimeZone(ctx, q)
Time Zone API

Return Location Object

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 

### Return type

[**Location**](location.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

