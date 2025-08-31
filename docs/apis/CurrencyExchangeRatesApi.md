# Brotal.FireflyIII.Api.CurrencyExchangeRatesApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteSpecificCurrencyExchangeRate**](CurrencyExchangeRatesApi.md#deletespecificcurrencyexchangerate) | **DELETE** /v1/exchange-rates/{id} | Delete a specific currency exchange rate. |
| [**DeleteSpecificCurrencyExchangeRateOnDate**](CurrencyExchangeRatesApi.md#deletespecificcurrencyexchangerateondate) | **DELETE** /v1/exchange-rates/{from}/{to}/{date} | Delete the currency exchange rate from &#39;from&#39; to &#39;to&#39; on the specified date. |
| [**DeleteSpecificCurrencyExchangeRates**](CurrencyExchangeRatesApi.md#deletespecificcurrencyexchangerates) | **DELETE** /v1/exchange-rates/{from}/{to} | Deletes ALL currency exchange rates from &#39;from&#39; to &#39;to&#39;. |
| [**ListCurrencyExchangeRates**](CurrencyExchangeRatesApi.md#listcurrencyexchangerates) | **GET** /v1/exchange-rates | List all exchange rates that Firefly III knows. |
| [**ListSpecificCurrencyExchangeRate**](CurrencyExchangeRatesApi.md#listspecificcurrencyexchangerate) | **GET** /v1/exchange-rates/{id} | List a single specific exchange rate. |
| [**ListSpecificCurrencyExchangeRateOnDate**](CurrencyExchangeRatesApi.md#listspecificcurrencyexchangerateondate) | **GET** /v1/exchange-rates/{from}/{to}/{date} | List the exchange rate for the from and to-currency on the requested date. |
| [**ListSpecificCurrencyExchangeRates**](CurrencyExchangeRatesApi.md#listspecificcurrencyexchangerates) | **GET** /v1/exchange-rates/{from}/{to} | List all exchange rates from/to the mentioned currencies. |
| [**StoreCurrencyExchangeRate**](CurrencyExchangeRatesApi.md#storecurrencyexchangerate) | **POST** /v1/exchange-rates | Store a new currency exchange rate. |
| [**StoreCurrencyExchangeRatesByDate**](CurrencyExchangeRatesApi.md#storecurrencyexchangeratesbydate) | **POST** /v1/exchange-rates/by-date/{date} | Store new currency exchange rates under this date |
| [**StoreCurrencyExchangeRatesByPair**](CurrencyExchangeRatesApi.md#storecurrencyexchangeratesbypair) | **POST** /v1/exchange-rates/by-currencies/{from}/{to} | Store new currency exchange rates under this from/to pair. |
| [**UpdateCurrencyExchangeRate**](CurrencyExchangeRatesApi.md#updatecurrencyexchangerate) | **PUT** /v1/exchange-rates/{id} | Update existing currency exchange rate. |
| [**UpdateCurrencyExchangeRateByDate**](CurrencyExchangeRatesApi.md#updatecurrencyexchangeratebydate) | **PUT** /v1/exchange-rates/{from}/{to}/{date} | Update existing currency exchange rate. |

<a id="deletespecificcurrencyexchangerate"></a>
# **DeleteSpecificCurrencyExchangeRate**
> void DeleteSpecificCurrencyExchangeRate (string id, Guid xTraceId = null)

Delete a specific currency exchange rate.

Delete a specific currency exchange rate by its internal ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the requested currency exchange rate. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

void (empty response body)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Currency exchange rate deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletespecificcurrencyexchangerateondate"></a>
# **DeleteSpecificCurrencyExchangeRateOnDate**
> void DeleteSpecificCurrencyExchangeRateOnDate (string from, string to, string date, Guid xTraceId = null)

Delete the currency exchange rate from 'from' to 'to' on the specified date.

Delete the currency exchange rate from 'from' to 'to' on the specified date.  It's important to know that the reverse exchange rate (from 'to' to 'from') will not be deleted and Firefly III will still be able to infer the correct exchange rate from the reverse one.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **from** | **string** | The currency code of the &#39;from&#39; currency. |  |
| **to** | **string** | The currency code of the &#39;to&#39; currency. |  |
| **date** | **string** |  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

void (empty response body)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Currency exchange rate(s) deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletespecificcurrencyexchangerates"></a>
# **DeleteSpecificCurrencyExchangeRates**
> void DeleteSpecificCurrencyExchangeRates (string from, string to, Guid xTraceId = null)

Deletes ALL currency exchange rates from 'from' to 'to'.

Deletes ALL currency exchange rates from 'from' to 'to'. It's important to know that the reverse exchange rates (from 'to' to 'from') will not be deleted and Firefly III will still be able to infer the correct exchange rate from the reverse one.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **from** | **string** | The currency code of the &#39;from&#39; currency. |  |
| **to** | **string** | The currency code of the &#39;to&#39; currency. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

void (empty response body)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Currency exchange rate(s) deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listcurrencyexchangerates"></a>
# **ListCurrencyExchangeRates**
> CurrencyExchangeRateArray ListCurrencyExchangeRates (Guid xTraceId = null, int limit = null, int page = null)

List all exchange rates that Firefly III knows.

List exchange rates that Firefly III knows.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**CurrencyExchangeRateArray**](CurrencyExchangeRateArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of all available currency exchange rates. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listspecificcurrencyexchangerate"></a>
# **ListSpecificCurrencyExchangeRate**
> CurrencyExchangeRateSingle ListSpecificCurrencyExchangeRate (string id, Guid xTraceId = null, int limit = null, int page = null)

List a single specific exchange rate.

List a single specific exchange rate by its ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the requested currency exchange rate. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**CurrencyExchangeRateSingle**](CurrencyExchangeRateSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The exchange rate requested. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listspecificcurrencyexchangerateondate"></a>
# **ListSpecificCurrencyExchangeRateOnDate**
> CurrencyExchangeRateArray ListSpecificCurrencyExchangeRateOnDate (string from, string to, string date, Guid xTraceId = null, int limit = null, int page = null)

List the exchange rate for the from and to-currency on the requested date.

List the exchange rate for the from and to-currency on the requested date.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **from** | **string** | The currency code of the &#39;from&#39; currency. |  |
| **to** | **string** | The currency code of the &#39;to&#39; currency. |  |
| **date** | **string** |  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**CurrencyExchangeRateArray**](CurrencyExchangeRateArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of currency exchange rates. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listspecificcurrencyexchangerates"></a>
# **ListSpecificCurrencyExchangeRates**
> CurrencyExchangeRateArray ListSpecificCurrencyExchangeRates (string from, string to, Guid xTraceId = null, int limit = null, int page = null)

List all exchange rates from/to the mentioned currencies.

List all exchange rates from/to the mentioned currencies.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **from** | **string** | The currency code of the &#39;from&#39; currency. |  |
| **to** | **string** | The currency code of the &#39;to&#39; currency. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**CurrencyExchangeRateArray**](CurrencyExchangeRateArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of currency exchange rates. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="storecurrencyexchangerate"></a>
# **StoreCurrencyExchangeRate**
> CurrencyExchangeRateSingle StoreCurrencyExchangeRate (CurrencyExchangeRateStore currencyExchangeRateStore, Guid xTraceId = null)

Store a new currency exchange rate.

Stores a new exchange rate. The data required can be submitted as a JSON body or as a list of parameters.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **currencyExchangeRateStore** | [**CurrencyExchangeRateStore**](CurrencyExchangeRateStore.md) | JSON array or key&#x3D;value pairs with the necessary exchange rate information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencyExchangeRateSingle**](CurrencyExchangeRateSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New exchange stored, result in response. If a rate already exists for this currency pair and date, it will be updated. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="storecurrencyexchangeratesbydate"></a>
# **StoreCurrencyExchangeRatesByDate**
> CurrencyExchangeRateArray StoreCurrencyExchangeRatesByDate (string date, CurrencyExchangeRateStoreByDate currencyExchangeRateStoreByDate, Guid xTraceId = null)

Store new currency exchange rates under this date

Stores a new set of exchange rates. The date is fixed (in the URL parameter) and the data required can be submitted as a JSON body.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **date** | **string** |  |  |
| **currencyExchangeRateStoreByDate** | [**CurrencyExchangeRateStoreByDate**](CurrencyExchangeRateStoreByDate.md) | JSON array with the necessary currency exchange rate information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencyExchangeRateArray**](CurrencyExchangeRateArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New exchange rates stored, result in response. If a rate already existed for any submitted entry, it will be updated. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="storecurrencyexchangeratesbypair"></a>
# **StoreCurrencyExchangeRatesByPair**
> CurrencyExchangeRateArray StoreCurrencyExchangeRatesByPair (string from, string to, Dictionary<string, string> requestBody, Guid xTraceId = null)

Store new currency exchange rates under this from/to pair.

Stores a new set of exchange rates for this pair. The date is variable, and the data required can be submitted as a JSON body.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **from** | **string** | The currency code of the &#39;from&#39; currency. |  |
| **to** | **string** | The currency code of the &#39;to&#39; currency. |  |
| **requestBody** | [**Dictionary&lt;string, string&gt;**](string.md) | JSON array with the necessary currency exchange rate information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencyExchangeRateArray**](CurrencyExchangeRateArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New exchange rates stored, result in response. If a rate already existed for any submitted entry, it will be updated. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatecurrencyexchangerate"></a>
# **UpdateCurrencyExchangeRate**
> CurrencyExchangeRateSingle UpdateCurrencyExchangeRate (string id, CurrencyExchangeRateUpdate currencyExchangeRateUpdate, Guid xTraceId = null)

Update existing currency exchange rate.

Used to update a single currency exchange rate by its ID. Including the from/to currency is optional. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the currency exchange rate. |  |
| **currencyExchangeRateUpdate** | [**CurrencyExchangeRateUpdate**](CurrencyExchangeRateUpdate.md) | JSON array or form-data with updated exchange rate information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencyExchangeRateSingle**](CurrencyExchangeRateSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated exchange rate stored, result in response |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatecurrencyexchangeratebydate"></a>
# **UpdateCurrencyExchangeRateByDate**
> CurrencyExchangeRateSingle UpdateCurrencyExchangeRateByDate (string from, string to, string date, CurrencyExchangeRateUpdateNoDate currencyExchangeRateUpdateNoDate, Guid xTraceId = null)

Update existing currency exchange rate.

Used to update a single currency exchange rate by its currency codes and date 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **from** | **string** | The currency code of the &#39;from&#39; currency. |  |
| **to** | **string** | The currency code of the &#39;to&#39; currency. |  |
| **date** | **string** |  |  |
| **currencyExchangeRateUpdateNoDate** | [**CurrencyExchangeRateUpdateNoDate**](CurrencyExchangeRateUpdateNoDate.md) | JSON array or form-data with updated exchange rate information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencyExchangeRateSingle**](CurrencyExchangeRateSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated exchange rate stored, result in response |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

