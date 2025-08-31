# Brotal.FireflyIII.Api.DataApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BulkUpdateTransactions**](DataApi.md#bulkupdatetransactions) | **POST** /v1/data/bulk/transactions | Bulk update transaction properties. For more information, see https://docs.firefly-iii.org/references/firefly-iii/api/specials/ |
| [**DestroyData**](DataApi.md#destroydata) | **DELETE** /v1/data/destroy | Endpoint to destroy user data |
| [**ExportAccounts**](DataApi.md#exportaccounts) | **GET** /v1/data/export/accounts | Export account data from Firefly III |
| [**ExportBills**](DataApi.md#exportbills) | **GET** /v1/data/export/bills | Export bills from Firefly III |
| [**ExportBudgets**](DataApi.md#exportbudgets) | **GET** /v1/data/export/budgets | Export budgets and budget amount data from Firefly III |
| [**ExportCategories**](DataApi.md#exportcategories) | **GET** /v1/data/export/categories | Export category data from Firefly III |
| [**ExportPiggies**](DataApi.md#exportpiggies) | **GET** /v1/data/export/piggy-banks | Export piggy banks from Firefly III |
| [**ExportRecurring**](DataApi.md#exportrecurring) | **GET** /v1/data/export/recurring | Export recurring transaction data from Firefly III |
| [**ExportRules**](DataApi.md#exportrules) | **GET** /v1/data/export/rules | Export rule groups and rule data from Firefly III |
| [**ExportTags**](DataApi.md#exporttags) | **GET** /v1/data/export/tags | Export tag data from Firefly III |
| [**ExportTransactions**](DataApi.md#exporttransactions) | **GET** /v1/data/export/transactions | Export transaction data from Firefly III |
| [**PurgeData**](DataApi.md#purgedata) | **DELETE** /v1/data/purge | Endpoint to purge user data |

<a id="bulkupdatetransactions"></a>
# **BulkUpdateTransactions**
> void BulkUpdateTransactions (string query, Guid xTraceId = null)

Bulk update transaction properties. For more information, see https://docs.firefly-iii.org/references/firefly-iii/api/specials/

Allows you to update transactions in bulk. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | The JSON query. |  |
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
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **204** | Empty response when the update was successful. A future improvement is to include the changed transactions. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="destroydata"></a>
# **DestroyData**
> void DestroyData (DataDestroyObject objects, Guid xTraceId = null)

Endpoint to destroy user data

A call to this endpoint deletes the requested data type. Use it with care and always with user permission. The demo user is incapable of using this endpoint. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **objects** | **DataDestroyObject** | The type of data that you wish to destroy. You can only use one at a time. |  |
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
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **204** | Empty response when data has been destroyed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exportaccounts"></a>
# **ExportAccounts**
> System.IO.Stream ExportAccounts (Guid xTraceId = null, ExportFileFilter type = null)

Export account data from Firefly III

This endpoint allows you to export your accounts from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exportbills"></a>
# **ExportBills**
> System.IO.Stream ExportBills (Guid xTraceId = null, ExportFileFilter type = null)

Export bills from Firefly III

This endpoint allows you to export your bills from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exportbudgets"></a>
# **ExportBudgets**
> System.IO.Stream ExportBudgets (Guid xTraceId = null, ExportFileFilter type = null)

Export budgets and budget amount data from Firefly III

This endpoint allows you to export your budgets and associated budget data from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exportcategories"></a>
# **ExportCategories**
> System.IO.Stream ExportCategories (Guid xTraceId = null, ExportFileFilter type = null)

Export category data from Firefly III

This endpoint allows you to export your categories from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exportpiggies"></a>
# **ExportPiggies**
> System.IO.Stream ExportPiggies (Guid xTraceId = null, ExportFileFilter type = null)

Export piggy banks from Firefly III

This endpoint allows you to export your piggy banks from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exportrecurring"></a>
# **ExportRecurring**
> System.IO.Stream ExportRecurring (Guid xTraceId = null, ExportFileFilter type = null)

Export recurring transaction data from Firefly III

This endpoint allows you to export your recurring transactions from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exportrules"></a>
# **ExportRules**
> System.IO.Stream ExportRules (Guid xTraceId = null, ExportFileFilter type = null)

Export rule groups and rule data from Firefly III

This endpoint allows you to export your rules and rule groups from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exporttags"></a>
# **ExportTags**
> System.IO.Stream ExportTags (Guid xTraceId = null, ExportFileFilter type = null)

Export tag data from Firefly III

This endpoint allows you to export your tags from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exporttransactions"></a>
# **ExportTransactions**
> System.IO.Stream ExportTransactions (DateOnly start, DateOnly end, Guid xTraceId = null, string accounts = null, ExportFileFilter type = null)

Export transaction data from Firefly III

This endpoint allows you to export transactions from Firefly III into a file. Currently supports CSV exports only. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | **string** | Limit the export of transactions to these accounts only. Only asset accounts will be accepted. Other types will be silently dropped.  | [optional]  |
| **type** | **ExportFileFilter** | The file type the export file (CSV is currently the only option). | [optional]  |

### Return type

**System.IO.Stream**

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/octet-stream


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | The exported transaction in a file. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="purgedata"></a>
# **PurgeData**
> void PurgeData (Guid xTraceId = null)

Endpoint to purge user data

A call to this endpoint purges all previously deleted data. Use it with care and always with user permission. The demo user is incapable of using this endpoint. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
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
| **401** | Unauthenticated |  -  |
| **400** | Bad request |  -  |
| **404** | Page not found |  -  |
| **500** | Internal exception |  -  |
| **204** | Empty response when data has been purged. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

