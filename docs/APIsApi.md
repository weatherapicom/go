# {{classname}}

All URIs are relative to *https://api.weatherapi.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Astronomy**](APIsApi.md#Astronomy) | **Get** /astronomy.json | Astronomy API
[**ForecastWeather**](APIsApi.md#ForecastWeather) | **Get** /forecast.json | Forecast API
[**FutureWeather**](APIsApi.md#FutureWeather) | **Get** /future.json | Future API
[**HistoryWeather**](APIsApi.md#HistoryWeather) | **Get** /history.json | History API
[**IpLookup**](APIsApi.md#IpLookup) | **Get** /ip.json | IP Lookup API
[**RealtimeWeather**](APIsApi.md#RealtimeWeather) | **Get** /current.json | Realtime API
[**SearchAutocompleteWeather**](APIsApi.md#SearchAutocompleteWeather) | **Get** /search.json | Search/Autocomplete API
[**TimeZone**](APIsApi.md#TimeZone) | **Get** /timezone.json | Time Zone API

# **Astronomy**
> InlineResponse2003 Astronomy(ctx, q, dt)
Astronomy API

Return Location and Astronomy Object

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 
  **dt** | **string**| Date on or after 1st Jan, 2015 in yyyy-MM-dd format | 

### Return type

[**InlineResponse2003**](inline_response_200_3.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ForecastWeather**
> InlineResponse2001 ForecastWeather(ctx, q, days, optional)
Forecast API

Forecast weather API method returns upto next 10 day weather forecast and weather alert as json. The data is returned as a Forecast Object.<br /><br />Forecast object contains astronomy data, day weather forecast and hourly interval weather information for a given city.

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


 **dt** | **optional.String**| Date should be between today and next 14 day in yyyy-MM-dd format. e.g. &#x27;2015-01-01&#x27; | 
 **unixdt** | **optional.Int32**| Please either pass &#x27;dt&#x27; or &#x27;unixdt&#x27; and not both in same request. unixdt should be between today and next 14 day in Unix format. e.g. 1490227200 | 
 **hour** | **optional.Int32**| Must be in 24 hour. For example 5 pm should be hour&#x3D;17, 6 am as hour&#x3D;6 | 
 **lang** | **optional.String**| Returns &#x27;condition:text&#x27; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#x27;lang-code&#x27;. | 

### Return type

[**InlineResponse2001**](inline_response_200_1.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FutureWeather**
> InlineResponse2002 FutureWeather(ctx, q, optional)
Future API

Future weather API method returns weather in a 3 hourly interval in future for a date between 14 days and 300 days from today in the future.

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
 **lang** | **optional.String**| Returns &#x27;condition:text&#x27; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#x27;lang-code&#x27;. | 

### Return type

[**InlineResponse2002**](inline_response_200_2.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **HistoryWeather**
> InlineResponse2002 HistoryWeather(ctx, q, dt, optional)
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


 **unixdt** | **optional.Int32**| Please either pass &#x27;dt&#x27; or &#x27;unixdt&#x27; and not both in same request.&lt;br /&gt;unixdt should be on or after 1st Jan, 2015 in Unix format | 
 **endDt** | **optional.String**| Date on or after 1st Jan, 2015 in yyyy-MM-dd format&lt;br /&gt;&#x27;end_dt&#x27; should be greater than &#x27;dt&#x27; parameter and difference should not be more than 30 days between the two dates. | 
 **unixendDt** | **optional.Int32**| Date on or after 1st Jan, 2015 in Unix Timestamp format&lt;br /&gt;unixend_dt has same restriction as &#x27;end_dt&#x27; parameter. Please either pass &#x27;end_dt&#x27; or &#x27;unixend_dt&#x27; and not both in same request. e.g. unixend_dt&#x3D;1490227200 | 
 **hour** | **optional.Int32**| Must be in 24 hour. For example 5 pm should be hour&#x3D;17, 6 am as hour&#x3D;6 | 
 **lang** | **optional.String**| Returns &#x27;condition:text&#x27; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#x27;lang-code&#x27;. | 

### Return type

[**InlineResponse2002**](inline_response_200_2.md)

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

# **RealtimeWeather**
> InlineResponse200 RealtimeWeather(ctx, q, optional)
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

 **lang** | **optional.String**| Returns &#x27;condition:text&#x27; field in API in the desired language.&lt;br /&gt; Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to check &#x27;lang-code&#x27;. | 

### Return type

[**InlineResponse200**](inline_response_200.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **SearchAutocompleteWeather**
> []Search SearchAutocompleteWeather(ctx, q)
Search/Autocomplete API

WeatherAPI.com Search or Autocomplete API returns matching cities and towns as an array of Location object.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **q** | **string**| Pass US Zipcode, UK Postcode, Canada Postalcode, IP address, Latitude/Longitude (decimal degree) or city name. Visit [request parameter section](https://www.weatherapi.com/docs/#intro-request) to learn more. | 

### Return type

[**[]Search**](array.md)

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

