# Brotal.FireflyIII.Api.SummaryApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetBasicSummary**](SummaryApi.md#getbasicsummary) | **GET** /v1/summary/basic | Returns basic sums of the users data. |

<a id="getbasicsummary"></a>
# **GetBasicSummary**
> Dictionary&lt;string, BasicSummaryEntry&gt; GetBasicSummary (DateOnly start, DateOnly end, Guid xTraceId = null, string currencyCode = null)

Returns basic sums of the users data.

Returns basic sums of the users data, like the net worth, spent and earned amounts. It is multi-currency, and is used in Firefly III to populate the dashboard. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **currencyCode** | **string** | A currency code like EUR or USD, to filter the result.  | [optional]  |

### Return type

[**Dictionary&lt;string, BasicSummaryEntry&gt;**](BasicSummaryEntry.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | An array of sums. It depends on the user what you can expect to get back, so please try this out on the demo site. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

