# Brotal.FireflyIII.Api.ChartsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetChartAccountOverview**](ChartsApi.md#getchartaccountoverview) | **GET** /v1/chart/account/overview | Dashboard chart with asset account balance information. |
| [**GetChartBalance**](ChartsApi.md#getchartbalance) | **GET** /v1/chart/balance/balance | Dashboard chart with balance information. |
| [**GetChartBudgetOverview**](ChartsApi.md#getchartbudgetoverview) | **GET** /v1/chart/budget/overview | Dashboard chart with budget information. |
| [**GetChartCategoryOverview**](ChartsApi.md#getchartcategoryoverview) | **GET** /v1/chart/category/overview | Dashboard chart with category information. |

<a id="getchartaccountoverview"></a>
# **GetChartAccountOverview**
> List&lt;ChartDataSet&gt; GetChartAccountOverview (DateOnly start, DateOnly end, Guid xTraceId = null)

Dashboard chart with asset account balance information.

This endpoint returns the data required to generate a chart with basic asset account balance information. This is used on the dashboard. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**List&lt;ChartDataSet&gt;**](ChartDataSet.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **500** | Internal exception |  -  |
| **200** | Line chart oriented chart information. Check out the model for more details. Each entry is a line (or bar) in the chart. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getchartbalance"></a>
# **GetChartBalance**
> List&lt;ChartDataSet&gt; GetChartBalance (DateOnly start, DateOnly end, Guid xTraceId = null)

Dashboard chart with balance information.

This endpoint returns the data required to generate a chart with balance information. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**List&lt;ChartDataSet&gt;**](ChartDataSet.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **500** | Internal exception |  -  |
| **200** | Line chart oriented chart information. Check out the model for more details. Each entry is a line (or bar) in the chart. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getchartbudgetoverview"></a>
# **GetChartBudgetOverview**
> List&lt;ChartDataSet&gt; GetChartBudgetOverview (DateOnly start, DateOnly end, Guid xTraceId = null)

Dashboard chart with budget information.

This endpoint returns the data required to generate a chart with basic budget information. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**List&lt;ChartDataSet&gt;**](ChartDataSet.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **500** | Internal exception |  -  |
| **200** | Bar chart oriented chart information. Check out the model for more details. Each entry is a line (or bar) in the chart. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getchartcategoryoverview"></a>
# **GetChartCategoryOverview**
> List&lt;ChartDataSet&gt; GetChartCategoryOverview (DateOnly start, DateOnly end, Guid xTraceId = null)

Dashboard chart with category information.

This endpoint returns the data required to generate a chart with basic category information. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**List&lt;ChartDataSet&gt;**](ChartDataSet.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **500** | Internal exception |  -  |
| **200** | Line chart oriented chart information. Check out the model for more details. Each entry is a line (or bar) in the chart. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

