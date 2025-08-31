# Brotal.FireflyIII.Api.AutocompleteApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAccountsAC**](AutocompleteApi.md#getaccountsac) | **GET** /v1/autocomplete/accounts | Returns all accounts of the user returned in a basic auto-complete array. |
| [**GetBillsAC**](AutocompleteApi.md#getbillsac) | **GET** /v1/autocomplete/bills | Returns all bills of the user returned in a basic auto-complete array. |
| [**GetBudgetsAC**](AutocompleteApi.md#getbudgetsac) | **GET** /v1/autocomplete/budgets | Returns all budgets of the user returned in a basic auto-complete array. |
| [**GetCategoriesAC**](AutocompleteApi.md#getcategoriesac) | **GET** /v1/autocomplete/categories | Returns all categories of the user returned in a basic auto-complete array. |
| [**GetCurrenciesAC**](AutocompleteApi.md#getcurrenciesac) | **GET** /v1/autocomplete/currencies | Returns all currencies of the user returned in a basic auto-complete array. |
| [**GetCurrenciesCodeAC**](AutocompleteApi.md#getcurrenciescodeac) | **GET** /v1/autocomplete/currencies-with-code | Returns all currencies of the user returned in a basic auto-complete array. This endpoint is DEPRECATED and I suggest you DO NOT use it. |
| [**GetObjectGroupsAC**](AutocompleteApi.md#getobjectgroupsac) | **GET** /v1/autocomplete/object-groups | Returns all object groups of the user returned in a basic auto-complete array. |
| [**GetPiggiesAC**](AutocompleteApi.md#getpiggiesac) | **GET** /v1/autocomplete/piggy-banks | Returns all piggy banks of the user returned in a basic auto-complete array. |
| [**GetPiggiesBalanceAC**](AutocompleteApi.md#getpiggiesbalanceac) | **GET** /v1/autocomplete/piggy-banks-with-balance | Returns all piggy banks of the user returned in a basic auto-complete array. |
| [**GetRecurringAC**](AutocompleteApi.md#getrecurringac) | **GET** /v1/autocomplete/recurring | Returns all recurring transactions of the user returned in a basic auto-complete array. |
| [**GetRuleGroupsAC**](AutocompleteApi.md#getrulegroupsac) | **GET** /v1/autocomplete/rule-groups | Returns all rule groups of the user returned in a basic auto-complete array. |
| [**GetRulesAC**](AutocompleteApi.md#getrulesac) | **GET** /v1/autocomplete/rules | Returns all rules of the user returned in a basic auto-complete array. |
| [**GetTagAC**](AutocompleteApi.md#gettagac) | **GET** /v1/autocomplete/tags | Returns all tags of the user returned in a basic auto-complete array. |
| [**GetTransactionTypesAC**](AutocompleteApi.md#gettransactiontypesac) | **GET** /v1/autocomplete/transaction-types | Returns all transaction types returned in a basic auto-complete array. English only. |
| [**GetTransactionsAC**](AutocompleteApi.md#gettransactionsac) | **GET** /v1/autocomplete/transactions | Returns all transaction descriptions of the user returned in a basic auto-complete array. |
| [**GetTransactionsIDAC**](AutocompleteApi.md#gettransactionsidac) | **GET** /v1/autocomplete/transactions-with-id | Returns all transactions, complemented with their ID, of the user returned in a basic auto-complete array. This endpoint is DEPRECATED and I suggest you DO NOT use it. |

<a id="getaccountsac"></a>
# **GetAccountsAC**
> List&lt;AutocompleteAccount&gt; GetAccountsAC (Guid xTraceId = null, string query = null, int limit = null, string date = null, List<AccountTypeFilter> types = null)

Returns all accounts of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |
| **date** | **string** | If the account is an asset account or a liability, the autocomplete will also return the balance of the account on this date. | [optional]  |
| **types** | [**List&lt;AccountTypeFilter&gt;**](AccountTypeFilter.md) | Optional filter on the account type(s) used in the autocomplete. | [optional]  |

### Return type

[**List&lt;AutocompleteAccount&gt;**](AutocompleteAccount.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | A list of accounts with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getbillsac"></a>
# **GetBillsAC**
> List&lt;AutocompleteBill&gt; GetBillsAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all bills of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteBill&gt;**](AutocompleteBill.md)

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
| **200** | A list of bills with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getbudgetsac"></a>
# **GetBudgetsAC**
> List&lt;AutocompleteBudget&gt; GetBudgetsAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all budgets of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteBudget&gt;**](AutocompleteBudget.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **200** | A list of budgets with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcategoriesac"></a>
# **GetCategoriesAC**
> List&lt;AutocompleteCategory&gt; GetCategoriesAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all categories of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteCategory&gt;**](AutocompleteCategory.md)

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
| **200** | A list of categories with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcurrenciesac"></a>
# **GetCurrenciesAC**
> List&lt;AutocompleteCurrency&gt; GetCurrenciesAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all currencies of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteCurrency&gt;**](AutocompleteCurrency.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **200** | A list of currencies with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcurrenciescodeac"></a>
# **GetCurrenciesCodeAC**
> List&lt;AutocompleteCurrencyCode&gt; GetCurrenciesCodeAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all currencies of the user returned in a basic auto-complete array. This endpoint is DEPRECATED and I suggest you DO NOT use it.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteCurrencyCode&gt;**](AutocompleteCurrencyCode.md)

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
| **200** | A list of currencies with very basic information and the currency code between brackets. This endpoint is DEPRECATED and I suggest you DO NOT use it. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getobjectgroupsac"></a>
# **GetObjectGroupsAC**
> List&lt;AutocompleteObjectGroup&gt; GetObjectGroupsAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all object groups of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteObjectGroup&gt;**](AutocompleteObjectGroup.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **200** | A list of object groups with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getpiggiesac"></a>
# **GetPiggiesAC**
> List&lt;AutocompletePiggy&gt; GetPiggiesAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all piggy banks of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompletePiggy&gt;**](AutocompletePiggy.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **200** | A list of piggy banks with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getpiggiesbalanceac"></a>
# **GetPiggiesBalanceAC**
> List&lt;AutocompletePiggyBalance&gt; GetPiggiesBalanceAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all piggy banks of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompletePiggyBalance&gt;**](AutocompletePiggyBalance.md)

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
| **200** | A list of piggy banks with very basic balance information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getrecurringac"></a>
# **GetRecurringAC**
> List&lt;AutocompleteRecurrence&gt; GetRecurringAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all recurring transactions of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteRecurrence&gt;**](AutocompleteRecurrence.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **200** | A list of recurring transactions with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getrulegroupsac"></a>
# **GetRuleGroupsAC**
> List&lt;AutocompleteRuleGroup&gt; GetRuleGroupsAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all rule groups of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteRuleGroup&gt;**](AutocompleteRuleGroup.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **200** | A list of rule groups with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getrulesac"></a>
# **GetRulesAC**
> List&lt;AutocompleteRule&gt; GetRulesAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all rules of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteRule&gt;**](AutocompleteRule.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **200** | A list of rules with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettagac"></a>
# **GetTagAC**
> List&lt;AutocompleteTag&gt; GetTagAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all tags of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteTag&gt;**](AutocompleteTag.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | A list of tags with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettransactiontypesac"></a>
# **GetTransactionTypesAC**
> List&lt;AutocompleteTransactionType&gt; GetTransactionTypesAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all transaction types returned in a basic auto-complete array. English only.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteTransactionType&gt;**](AutocompleteTransactionType.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | A list of transaction types with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettransactionsac"></a>
# **GetTransactionsAC**
> List&lt;AutocompleteTransaction&gt; GetTransactionsAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all transaction descriptions of the user returned in a basic auto-complete array.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteTransaction&gt;**](AutocompleteTransaction.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | A list of transaction descriptions with very basic information. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettransactionsidac"></a>
# **GetTransactionsIDAC**
> List&lt;AutocompleteTransactionID&gt; GetTransactionsIDAC (Guid xTraceId = null, string query = null, int limit = null)

Returns all transactions, complemented with their ID, of the user returned in a basic auto-complete array. This endpoint is DEPRECATED and I suggest you DO NOT use it.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **query** | **string** | The autocomplete search query. | [optional]  |
| **limit** | **int** | The number of items returned. | [optional]  |

### Return type

[**List&lt;AutocompleteTransactionID&gt;**](AutocompleteTransactionID.md)

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
| **422** | Validation error. The body will have the exact details. |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | A list of transactions with very basic information. This endpoint is DEPRECATED and I suggest you DO NOT use it. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

