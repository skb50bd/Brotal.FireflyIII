# Brotal.FireflyIII.Api.AvailableBudgetsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAvailableBudget**](AvailableBudgetsApi.md#getavailablebudget) | **GET** /v1/available-budgets/{id} | Get a single available budget. |
| [**ListAvailableBudgets**](AvailableBudgetsApi.md#listavailablebudgets) | **GET** /v1/available-budgets | List all available budget amounts. |

<a id="getavailablebudget"></a>
# **GetAvailableBudget**
> AvailableBudgetSingle GetAvailableBudget (string id, Guid xTraceId = null)

Get a single available budget.

Get a single available budget, by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the available budget. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**AvailableBudgetSingle**](AvailableBudgetSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/vnd.api+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The requested available budget |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listavailablebudgets"></a>
# **ListAvailableBudgets**
> AvailableBudgetArray ListAvailableBudgets (Guid xTraceId = null, int limit = null, int page = null, DateOnly start = null, DateOnly end = null)

List all available budget amounts.

Firefly III calculates the total amount of money budgeted in so-called \"available budgets\". This endpoint returns all of these amounts and the periods for which they are calculated. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  | [optional]  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  | [optional]  |

### Return type

[**AvailableBudgetArray**](AvailableBudgetArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/vnd.api+json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | A list of available budget amounts. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

