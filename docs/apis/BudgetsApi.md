# Brotal.FireflyIII.Api.BudgetsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteBudget**](BudgetsApi.md#deletebudget) | **DELETE** /v1/budgets/{id} | Delete a budget. |
| [**DeleteBudgetLimit**](BudgetsApi.md#deletebudgetlimit) | **DELETE** /v1/budgets/{id}/limits/{limitId} | Delete a budget limit. |
| [**GetBudget**](BudgetsApi.md#getbudget) | **GET** /v1/budgets/{id} | Get a single budget. |
| [**GetBudgetLimit**](BudgetsApi.md#getbudgetlimit) | **GET** /v1/budgets/{id}/limits/{limitId} | Get single budget limit. |
| [**ListAttachmentByBudget**](BudgetsApi.md#listattachmentbybudget) | **GET** /v1/budgets/{id}/attachments | Lists all attachments of a budget. |
| [**ListBudget**](BudgetsApi.md#listbudget) | **GET** /v1/budgets | List all budgets. |
| [**ListBudgetLimit**](BudgetsApi.md#listbudgetlimit) | **GET** /v1/budget-limits | Get list of budget limits by date |
| [**ListBudgetLimitByBudget**](BudgetsApi.md#listbudgetlimitbybudget) | **GET** /v1/budgets/{id}/limits | Get all limits for a budget. |
| [**ListTransactionByBudget**](BudgetsApi.md#listtransactionbybudget) | **GET** /v1/budgets/{id}/transactions | All transactions to a budget. |
| [**ListTransactionByBudgetLimit**](BudgetsApi.md#listtransactionbybudgetlimit) | **GET** /v1/budgets/{id}/limits/{limitId}/transactions | List all transactions by a budget limit ID. |
| [**ListTransactionWithoutBudget**](BudgetsApi.md#listtransactionwithoutbudget) | **GET** /v1/budgets/transactions-without-budget | All transactions without a budget. |
| [**StoreBudget**](BudgetsApi.md#storebudget) | **POST** /v1/budgets | Store a new budget |
| [**StoreBudgetLimit**](BudgetsApi.md#storebudgetlimit) | **POST** /v1/budgets/{id}/limits | Store new budget limit. |
| [**UpdateBudget**](BudgetsApi.md#updatebudget) | **PUT** /v1/budgets/{id} | Update existing budget. |
| [**UpdateBudgetLimit**](BudgetsApi.md#updatebudgetlimit) | **PUT** /v1/budgets/{id}/limits/{limitId} | Update existing budget limit. |

<a id="deletebudget"></a>
# **DeleteBudget**
> void DeleteBudget (string id, Guid xTraceId = null)

Delete a budget.

Delete a budget. Transactions will not be deleted.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. |  |
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
| **204** | Budget deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletebudgetlimit"></a>
# **DeleteBudgetLimit**
> void DeleteBudgetLimit (string id, string limitId, Guid xTraceId = null)

Delete a budget limit.

Delete a budget limit.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. The budget limit MUST be associated to the budget ID. |  |
| **limitId** | **string** | The ID of the budget limit. The budget limit MUST be associated to the budget ID. |  |
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
| **204** | Budget limit deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getbudget"></a>
# **GetBudget**
> BudgetSingle GetBudget (string id, Guid xTraceId = null, DateOnly start = null, DateOnly end = null)

Get a single budget.

Get a single budget. If the start date and end date are submitted as well, the \"spent\" array will be updated accordingly.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the requested budget. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **start** | **DateOnly** | A date formatted YYYY-MM-DD, to get info on how much the user has spent.  | [optional]  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD, to get info on how much the user has spent.  | [optional]  |

### Return type

[**BudgetSingle**](BudgetSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The requested budget |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getbudgetlimit"></a>
# **GetBudgetLimit**
> BudgetLimitSingle GetBudgetLimit (string id, int limitId, Guid xTraceId = null)

Get single budget limit.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. The budget limit MUST be associated to the budget ID. |  |
| **limitId** | **int** | The ID of the budget limit. The budget limit MUST be associated to the budget ID. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**BudgetLimitSingle**](BudgetLimitSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The requested budget limit |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listattachmentbybudget"></a>
# **ListAttachmentByBudget**
> AttachmentArray ListAttachmentByBudget (string id, Guid xTraceId = null, int limit = null, int page = null)

Lists all attachments of a budget.

Lists all attachments.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**AttachmentArray**](AttachmentArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of attachments |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listbudget"></a>
# **ListBudget**
> BudgetArray ListBudget (Guid xTraceId = null, int limit = null, int page = null, DateOnly start = null, DateOnly end = null)

List all budgets.

List all the budgets the user has made. If the start date and end date are submitted as well, the \"spent\" array will be updated accordingly.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **start** | **DateOnly** | A date formatted YYYY-MM-DD, to get info on how much the user has spent. You must submit both start and end.  | [optional]  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD, to get info on how much the user has spent. You must submit both start and end.  | [optional]  |

### Return type

[**BudgetArray**](BudgetArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of budgets. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listbudgetlimit"></a>
# **ListBudgetLimit**
> BudgetLimitArray ListBudgetLimit (DateOnly start, DateOnly end, Guid xTraceId = null)

Get list of budget limits by date

Get all budget limits for for this date range. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**BudgetLimitArray**](BudgetLimitArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of budget limits. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listbudgetlimitbybudget"></a>
# **ListBudgetLimitByBudget**
> BudgetLimitArray ListBudgetLimitByBudget (string id, Guid xTraceId = null, DateOnly start = null, DateOnly end = null)

Get all limits for a budget.

Get all budget limits for this budget and the money spent, and money left. You can limit the list by submitting a date range as well. The \"spent\" array for each budget limit is NOT influenced by the start and end date of your query, but by the start and end date of the budget limit itself. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the requested budget. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  | [optional]  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  | [optional]  |

### Return type

[**BudgetLimitArray**](BudgetLimitArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of budget limits applicable to this budget. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listtransactionbybudget"></a>
# **ListTransactionByBudget**
> TransactionArray ListTransactionByBudget (string id, Guid xTraceId = null, int limit = null, int page = null, DateOnly start = null, DateOnly end = null, TransactionTypeFilter type = null)

All transactions to a budget.

Get all transactions linked to a budget, possibly limited by start and end


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  | [optional]  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  | [optional]  |
| **type** | **TransactionTypeFilter** | Optional filter on the transaction type(s) returned | [optional]  |

### Return type

[**TransactionArray**](TransactionArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of transactions. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listtransactionbybudgetlimit"></a>
# **ListTransactionByBudgetLimit**
> TransactionArray ListTransactionByBudgetLimit (string id, string limitId, Guid xTraceId = null, int limit = null, int page = null, TransactionTypeFilter type = null)

List all transactions by a budget limit ID.

List all the transactions within one budget limit. The start and end date are dictated by the budget limit.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. The budget limit MUST be associated to the budget ID. |  |
| **limitId** | **string** | The ID of the budget limit. The budget limit MUST be associated to the budget ID. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **type** | **TransactionTypeFilter** | Optional filter on the transaction type(s) returned | [optional]  |

### Return type

[**TransactionArray**](TransactionArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of transactions. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listtransactionwithoutbudget"></a>
# **ListTransactionWithoutBudget**
> TransactionArray ListTransactionWithoutBudget (Guid xTraceId = null, int limit = null, int page = null, DateOnly start = null, DateOnly end = null)

All transactions without a budget.

Get all transactions NOT linked to a budget, possibly limited by start and end


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  | [optional]  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  | [optional]  |

### Return type

[**TransactionArray**](TransactionArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of transactions. |  -  |
| **401** | Unauthenticated |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="storebudget"></a>
# **StoreBudget**
> BudgetSingle StoreBudget (BudgetStore budgetStore, Guid xTraceId = null)

Store a new budget

Creates a new budget. The data required can be submitted as a JSON body or as a list of parameters.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **budgetStore** | [**BudgetStore**](BudgetStore.md) | JSON array or key&#x3D;value pairs with the necessary budget information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**BudgetSingle**](BudgetSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New budget stored, result in response. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="storebudgetlimit"></a>
# **StoreBudgetLimit**
> BudgetLimitSingle StoreBudgetLimit (string id, BudgetLimitStore budgetLimitStore, Guid xTraceId = null)

Store new budget limit.

Store a new budget limit under this budget.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. |  |
| **budgetLimitStore** | [**BudgetLimitStore**](BudgetLimitStore.md) | JSON array or key&#x3D;value pairs with the necessary budget information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**BudgetLimitSingle**](BudgetLimitSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New budget limit stored, result in response. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatebudget"></a>
# **UpdateBudget**
> BudgetSingle UpdateBudget (string id, BudgetUpdate budgetUpdate, Guid xTraceId = null)

Update existing budget.

Update existing budget. This endpoint cannot be used to set budget amount limits.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. |  |
| **budgetUpdate** | [**BudgetUpdate**](BudgetUpdate.md) | JSON array with updated budget information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**BudgetSingle**](BudgetSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated budget stored, result in response |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatebudgetlimit"></a>
# **UpdateBudgetLimit**
> BudgetLimitSingle UpdateBudgetLimit (string id, string limitId, BudgetLimitUpdate budgetLimitUpdate, Guid xTraceId = null)

Update existing budget limit.

Update existing budget limit.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the budget. The budget limit MUST be associated to the budget ID. |  |
| **limitId** | **string** | The ID of the budget limit. The budget limit MUST be associated to the budget ID. |  |
| **budgetLimitUpdate** | [**BudgetLimitUpdate**](BudgetLimitUpdate.md) | JSON array with updated budget limit information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**BudgetLimitSingle**](BudgetLimitSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated budget limit stored, result in response |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

