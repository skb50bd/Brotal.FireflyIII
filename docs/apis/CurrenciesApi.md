# Brotal.FireflyIII.Api.CurrenciesApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteCurrency**](CurrenciesApi.md#deletecurrency) | **DELETE** /v1/currencies/{code} | Delete a currency. |
| [**DisableCurrency**](CurrenciesApi.md#disablecurrency) | **POST** /v1/currencies/{code}/disable | Disable a currency. |
| [**EnableCurrency**](CurrenciesApi.md#enablecurrency) | **POST** /v1/currencies/{code}/enable | Enable a single currency. |
| [**GetCurrency**](CurrenciesApi.md#getcurrency) | **GET** /v1/currencies/{code} | Get a single currency. |
| [**GetPrimaryCurrency**](CurrenciesApi.md#getprimarycurrency) | **GET** /v1/currencies/primary | Get the primary currency of the current administration. |
| [**ListAccountByCurrency**](CurrenciesApi.md#listaccountbycurrency) | **GET** /v1/currencies/{code}/accounts | List all accounts with this currency. |
| [**ListAvailableBudgetByCurrency**](CurrenciesApi.md#listavailablebudgetbycurrency) | **GET** /v1/currencies/{code}/available-budgets | List all available budgets with this currency. |
| [**ListBillByCurrency**](CurrenciesApi.md#listbillbycurrency) | **GET** /v1/currencies/{code}/bills | List all bills with this currency. |
| [**ListBudgetLimitByCurrency**](CurrenciesApi.md#listbudgetlimitbycurrency) | **GET** /v1/currencies/{code}/budget-limits | List all budget limits with this currency |
| [**ListCurrency**](CurrenciesApi.md#listcurrency) | **GET** /v1/currencies | List all currencies. |
| [**ListRecurrenceByCurrency**](CurrenciesApi.md#listrecurrencebycurrency) | **GET** /v1/currencies/{code}/recurrences | List all recurring transactions with this currency. |
| [**ListRuleByCurrency**](CurrenciesApi.md#listrulebycurrency) | **GET** /v1/currencies/{code}/rules | List all rules with this currency. |
| [**ListTransactionByCurrency**](CurrenciesApi.md#listtransactionbycurrency) | **GET** /v1/currencies/{code}/transactions | List all transactions with this currency. |
| [**PrimaryCurrency**](CurrenciesApi.md#primarycurrency) | **POST** /v1/currencies/{code}/primary | Make currency primary currency. |
| [**StoreCurrency**](CurrenciesApi.md#storecurrency) | **POST** /v1/currencies | Store a new currency |
| [**UpdateCurrency**](CurrenciesApi.md#updatecurrency) | **PUT** /v1/currencies/{code} | Update existing currency. |

<a id="deletecurrency"></a>
# **DeleteCurrency**
> void DeleteCurrency (string code, Guid xTraceId = null)

Delete a currency.

Delete a currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
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
| **204** | Currency deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="disablecurrency"></a>
# **DisableCurrency**
> CurrencySingle DisableCurrency (string code, Guid xTraceId = null)

Disable a currency.

Disable a currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencySingle**](CurrencySingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Currency was disabled. |  -  |
| **409** | Currency cannot be disabled, because it is still in use. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="enablecurrency"></a>
# **EnableCurrency**
> CurrencySingle EnableCurrency (string code, Guid xTraceId = null)

Enable a single currency.

Enable a single currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencySingle**](CurrencySingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Currency was enabled. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcurrency"></a>
# **GetCurrency**
> CurrencySingle GetCurrency (string code, Guid xTraceId = null)

Get a single currency.

Get a single currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencySingle**](CurrencySingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The requested currency |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getprimarycurrency"></a>
# **GetPrimaryCurrency**
> CurrencySingle GetPrimaryCurrency (Guid xTraceId = null)

Get the primary currency of the current administration.

Get the primary currency of the current administration. This replaces what was called \"the user's default currency\" although they are essentially the same.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencySingle**](CurrencySingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The primary currency |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listaccountbycurrency"></a>
# **ListAccountByCurrency**
> AccountArray ListAccountByCurrency (string code, Guid xTraceId = null, int limit = null, int page = null, DateOnly date = null, AccountTypeFilter type = null)

List all accounts with this currency.

List all accounts with this currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **date** | **DateOnly** | A date formatted YYYY-MM-DD. When added to the request, Firefly III will show the account&#39;s balance on that day.  | [optional]  |
| **type** | **AccountTypeFilter** | Optional filter on the account type(s) returned | [optional]  |

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
| **200** | A list of accounts |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listavailablebudgetbycurrency"></a>
# **ListAvailableBudgetByCurrency**
> AvailableBudgetArray ListAvailableBudgetByCurrency (string code, Guid xTraceId = null, int limit = null, int page = null)

List all available budgets with this currency.

List all available budgets with this currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**AvailableBudgetArray**](AvailableBudgetArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of available budgets |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listbillbycurrency"></a>
# **ListBillByCurrency**
> BillArray ListBillByCurrency (string code, Guid xTraceId = null, int limit = null, int page = null)

List all bills with this currency.

List all bills with this currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**BillArray**](BillArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of bills. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listbudgetlimitbycurrency"></a>
# **ListBudgetLimitByCurrency**
> BudgetLimitArray ListBudgetLimitByCurrency (string code, Guid xTraceId = null, int limit = null, int page = null, DateOnly start = null, DateOnly end = null)

List all budget limits with this currency

List all budget limits with this currency


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **start** | **DateOnly** | Start date for the budget limit list. | [optional]  |
| **end** | **DateOnly** | End date for the budget limit list. | [optional]  |

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

<a id="listcurrency"></a>
# **ListCurrency**
> CurrencyArray ListCurrency (Guid xTraceId = null, int limit = null, int page = null)

List all currencies.

List all currencies.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**CurrencyArray**](CurrencyArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of currencies. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listrecurrencebycurrency"></a>
# **ListRecurrenceByCurrency**
> RecurrenceArray ListRecurrenceByCurrency (string code, Guid xTraceId = null, int limit = null, int page = null)

List all recurring transactions with this currency.

List all recurring transactions with this currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**RecurrenceArray**](RecurrenceArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of recurring transactions |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listrulebycurrency"></a>
# **ListRuleByCurrency**
> RuleArray ListRuleByCurrency (string code, Guid xTraceId = null, int limit = null, int page = null)

List all rules with this currency.

List all rules with this currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**RuleArray**](RuleArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of rules |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listtransactionbycurrency"></a>
# **ListTransactionByCurrency**
> TransactionArray ListTransactionByCurrency (string code, Guid xTraceId = null, int limit = null, int page = null, DateOnly start = null, DateOnly end = null, TransactionTypeFilter type = null)

List all transactions with this currency.

List all transactions with this currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **start** | **DateOnly** | A date formatted YYYY-MM-DD, to limit the list of transactions.  | [optional]  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD, to limit the list of transactions.  | [optional]  |
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

<a id="primarycurrency"></a>
# **PrimaryCurrency**
> CurrencySingle PrimaryCurrency (string code, Guid xTraceId = null)

Make currency primary currency.

Make this currency the primary currency for the current financial administration. If the currency is not enabled, it will be enabled as well.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencySingle**](CurrencySingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Currency has been made the primary currency. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="storecurrency"></a>
# **StoreCurrency**
> CurrencySingle StoreCurrency (CurrencyStore currencyStore, Guid xTraceId = null)

Store a new currency

Creates a new currency. The data required can be submitted as a JSON body or as a list of parameters.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **currencyStore** | [**CurrencyStore**](CurrencyStore.md) | JSON array or key&#x3D;value pairs with the necessary currency information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencySingle**](CurrencySingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New currency stored, result in response. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatecurrency"></a>
# **UpdateCurrency**
> CurrencySingle UpdateCurrency (string code, CurrencyUpdate currencyUpdate, Guid xTraceId = null)

Update existing currency.

Update existing currency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** | The currency code. |  |
| **currencyUpdate** | [**CurrencyUpdate**](CurrencyUpdate.md) | JSON array with updated currency information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**CurrencySingle**](CurrencySingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/vnd.api+json, application/x-www-form-urlencoded
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated currency stored, result in response |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

