# Brotal.FireflyIII.Api.SearchApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SearchAccounts**](SearchApi.md#searchaccounts) | **GET** /v1/search/accounts | Search for accounts |
| [**SearchTransactions**](SearchApi.md#searchtransactions) | **GET** /v1/search/transactions | Search for transactions |

<a id="searchaccounts"></a>
# **SearchAccounts**
> AccountArray SearchAccounts (string query, AccountSearchFieldFilter field, Guid xTraceId = null, int limit = null, int page = null, AccountTypeFilter type = null)

Search for accounts

Search for accounts


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | The query you wish to search for. |  |
| **field** | **AccountSearchFieldFilter** | The account field(s) you want to search in. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **type** | **AccountTypeFilter** | The type of accounts you wish to limit the search to. | [optional]  |

### Return type

[**AccountArray**](AccountArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of accounts. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchtransactions"></a>
# **SearchTransactions**
> TransactionArray SearchTransactions (string query, Guid xTraceId = null, int limit = null, int page = null)

Search for transactions

Searches through the users transactions.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | The query you wish to search for. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

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

