# Brotal.FireflyIII.Api.InsightApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**InsightExpenseAsset**](InsightApi.md#insightexpenseasset) | **GET** /v1/insight/expense/asset | Insight into expenses, grouped by asset account. |
| [**InsightExpenseBill**](InsightApi.md#insightexpensebill) | **GET** /v1/insight/expense/bill | Insight into expenses, grouped by bill. |
| [**InsightExpenseBudget**](InsightApi.md#insightexpensebudget) | **GET** /v1/insight/expense/budget | Insight into expenses, grouped by budget. |
| [**InsightExpenseCategory**](InsightApi.md#insightexpensecategory) | **GET** /v1/insight/expense/category | Insight into expenses, grouped by category. |
| [**InsightExpenseExpense**](InsightApi.md#insightexpenseexpense) | **GET** /v1/insight/expense/expense | Insight into expenses, grouped by expense account. |
| [**InsightExpenseNoBill**](InsightApi.md#insightexpensenobill) | **GET** /v1/insight/expense/no-bill | Insight into expenses, without bill. |
| [**InsightExpenseNoBudget**](InsightApi.md#insightexpensenobudget) | **GET** /v1/insight/expense/no-budget | Insight into expenses, without budget. |
| [**InsightExpenseNoCategory**](InsightApi.md#insightexpensenocategory) | **GET** /v1/insight/expense/no-category | Insight into expenses, without category. |
| [**InsightExpenseNoTag**](InsightApi.md#insightexpensenotag) | **GET** /v1/insight/expense/no-tag | Insight into expenses, without tag. |
| [**InsightExpenseTag**](InsightApi.md#insightexpensetag) | **GET** /v1/insight/expense/tag | Insight into expenses, grouped by tag. |
| [**InsightExpenseTotal**](InsightApi.md#insightexpensetotal) | **GET** /v1/insight/expense/total | Insight into total expenses. |
| [**InsightIncomeAsset**](InsightApi.md#insightincomeasset) | **GET** /v1/insight/income/asset | Insight into income, grouped by asset account. |
| [**InsightIncomeCategory**](InsightApi.md#insightincomecategory) | **GET** /v1/insight/income/category | Insight into income, grouped by category. |
| [**InsightIncomeNoCategory**](InsightApi.md#insightincomenocategory) | **GET** /v1/insight/income/no-category | Insight into income, without category. |
| [**InsightIncomeNoTag**](InsightApi.md#insightincomenotag) | **GET** /v1/insight/income/no-tag | Insight into income, without tag. |
| [**InsightIncomeRevenue**](InsightApi.md#insightincomerevenue) | **GET** /v1/insight/income/revenue | Insight into income, grouped by revenue account. |
| [**InsightIncomeTag**](InsightApi.md#insightincometag) | **GET** /v1/insight/income/tag | Insight into income, grouped by tag. |
| [**InsightIncomeTotal**](InsightApi.md#insightincometotal) | **GET** /v1/insight/income/total | Insight into total income. |
| [**InsightTransferCategory**](InsightApi.md#insighttransfercategory) | **GET** /v1/insight/transfer/category | Insight into transfers, grouped by category. |
| [**InsightTransferNoCategory**](InsightApi.md#insighttransfernocategory) | **GET** /v1/insight/transfer/no-category | Insight into transfers, without category. |
| [**InsightTransferNoTag**](InsightApi.md#insighttransfernotag) | **GET** /v1/insight/transfer/no-tag | Insight into expenses, without tag. |
| [**InsightTransferTag**](InsightApi.md#insighttransfertag) | **GET** /v1/insight/transfer/tag | Insight into transfers, grouped by tag. |
| [**InsightTransferTotal**](InsightApi.md#insighttransfertotal) | **GET** /v1/insight/transfer/total | Insight into total transfers. |
| [**InsightTransfers**](InsightApi.md#insighttransfers) | **GET** /v1/insight/transfer/asset | Insight into transfers, grouped by account. |

<a id="insightexpenseasset"></a>
# **InsightExpenseAsset**
> List&lt;InsightGroupEntry&gt; InsightExpenseAsset (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into expenses, grouped by asset account.

This endpoint gives a summary of the expenses made by the user, grouped by asset account. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of asset accounts and expense details. Each asset account has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensebill"></a>
# **InsightExpenseBill**
> List&lt;InsightGroupEntry&gt; InsightExpenseBill (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> bills = null, List<long> accounts = null)

Insight into expenses, grouped by bill.

This endpoint gives a summary of the expenses made by the user, grouped by (any) bill. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **bills** | [**List&lt;long&gt;**](long.md) | The bills to be included in the results.  | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of budget and expense details. Each budget has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensebudget"></a>
# **InsightExpenseBudget**
> List&lt;InsightGroupEntry&gt; InsightExpenseBudget (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> budgets = null, List<long> accounts = null)

Insight into expenses, grouped by budget.

This endpoint gives a summary of the expenses made by the user, grouped by (any) budget. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **budgets** | [**List&lt;long&gt;**](long.md) | The budgets to be included in the results.  | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of budget and expense details. Each budget has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensecategory"></a>
# **InsightExpenseCategory**
> List&lt;InsightGroupEntry&gt; InsightExpenseCategory (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> categories = null, List<long> accounts = null)

Insight into expenses, grouped by category.

This endpoint gives a summary of the expenses made by the user, grouped by (any) category. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **categories** | [**List&lt;long&gt;**](long.md) | The categories to be included in the results.  | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of category and expense details. Each category has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpenseexpense"></a>
# **InsightExpenseExpense**
> List&lt;InsightGroupEntry&gt; InsightExpenseExpense (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into expenses, grouped by expense account.

This endpoint gives a summary of the expenses made by the user, grouped by expense account. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you add the accounts ID&#39;s of expense accounts, only those accounts are included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. You can combine both asset / liability and expense account ID&#39;s. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of expense accounts and expense details. Each expense account has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensenobill"></a>
# **InsightExpenseNoBill**
> List&lt;InsightTotalEntry&gt; InsightExpenseNoBill (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into expenses, without bill.

This endpoint gives a summary of the expenses made by the user, including only expenses with no bill. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of expense details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensenobudget"></a>
# **InsightExpenseNoBudget**
> List&lt;InsightTotalEntry&gt; InsightExpenseNoBudget (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into expenses, without budget.

This endpoint gives a summary of the expenses made by the user, including only expenses with no budget. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of expense details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensenocategory"></a>
# **InsightExpenseNoCategory**
> List&lt;InsightTotalEntry&gt; InsightExpenseNoCategory (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into expenses, without category.

This endpoint gives a summary of the expenses made by the user, including only expenses with no category. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of expense details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensenotag"></a>
# **InsightExpenseNoTag**
> List&lt;InsightTotalEntry&gt; InsightExpenseNoTag (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into expenses, without tag.

This endpoint gives a summary of the expenses made by the user, including only expenses with no tag. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of expense details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensetag"></a>
# **InsightExpenseTag**
> List&lt;InsightGroupEntry&gt; InsightExpenseTag (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> tags = null, List<long> accounts = null)

Insight into expenses, grouped by tag.

This endpoint gives a summary of the expenses made by the user, grouped by (any) tag. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **tags** | [**List&lt;long&gt;**](long.md) | The tags to be included in the results.  | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of tag and expense details. Each tag has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightexpensetotal"></a>
# **InsightExpenseTotal**
> List&lt;InsightTotalEntry&gt; InsightExpenseTotal (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into total expenses.

This endpoint gives a sum of the total expenses made by the user. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only withdrawals from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of sums in different currencies. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightincomeasset"></a>
# **InsightIncomeAsset**
> List&lt;InsightGroupEntry&gt; InsightIncomeAsset (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into income, grouped by asset account.

This endpoint gives a summary of the income received by the user, grouped by asset account. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of asset accounts and income details. Each asset account has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightincomecategory"></a>
# **InsightIncomeCategory**
> List&lt;InsightGroupEntry&gt; InsightIncomeCategory (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> categories = null, List<long> accounts = null)

Insight into income, grouped by category.

This endpoint gives a summary of the income received by the user, grouped by (any) category. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **categories** | [**List&lt;long&gt;**](long.md) | The categories to be included in the results.  | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of category and income details. Each category has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightincomenocategory"></a>
# **InsightIncomeNoCategory**
> List&lt;InsightTotalEntry&gt; InsightIncomeNoCategory (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into income, without category.

This endpoint gives a summary of the income received by the user, including only income with no category. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of income details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightincomenotag"></a>
# **InsightIncomeNoTag**
> List&lt;InsightTotalEntry&gt; InsightIncomeNoTag (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into income, without tag.

This endpoint gives a summary of the income received by the user, including only income with no tag. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of income details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightincomerevenue"></a>
# **InsightIncomeRevenue**
> List&lt;InsightGroupEntry&gt; InsightIncomeRevenue (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into income, grouped by revenue account.

This endpoint gives a summary of the income received by the user, grouped by revenue account. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you add the accounts ID&#39;s of revenue accounts, only those accounts are included in the results. If you include ID&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. You can combine both asset / liability and deposit account ID&#39;s. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of revenue accounts and income details. Each revenue account has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightincometag"></a>
# **InsightIncomeTag**
> List&lt;InsightGroupEntry&gt; InsightIncomeTag (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> tags = null, List<long> accounts = null)

Insight into income, grouped by tag.

This endpoint gives a summary of the income received by the user, grouped by (any) tag. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **tags** | [**List&lt;long&gt;**](long.md) | The tags to be included in the results.  | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of tag and income details. Each tag has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insightincometotal"></a>
# **InsightIncomeTotal**
> List&lt;InsightTotalEntry&gt; InsightIncomeTotal (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into total income.

This endpoint gives a sum of the total income received by the user. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only deposits to those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of sums in different currencies. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insighttransfercategory"></a>
# **InsightTransferCategory**
> List&lt;InsightGroupEntry&gt; InsightTransferCategory (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> categories = null, List<long> accounts = null)

Insight into transfers, grouped by category.

This endpoint gives a summary of the transfers made by the user, grouped by (any) category. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **categories** | [**List&lt;long&gt;**](long.md) | The categories to be included in the results.  | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of category and transfer details. Each category has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insighttransfernocategory"></a>
# **InsightTransferNoCategory**
> List&lt;InsightTotalEntry&gt; InsightTransferNoCategory (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into transfers, without category.

This endpoint gives a summary of the transfers made by the user, including only transfers with no category. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of transfer details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insighttransfernotag"></a>
# **InsightTransferNoTag**
> List&lt;InsightTotalEntry&gt; InsightTransferNoTag (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into expenses, without tag.

This endpoint gives a summary of the transfers made by the user, including only transfers with no tag. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only transfers from those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of transfer details. One row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insighttransfertag"></a>
# **InsightTransferTag**
> List&lt;InsightGroupEntry&gt; InsightTransferTag (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> tags = null, List<long> accounts = null)

Insight into transfers, grouped by tag.

This endpoint gives a summary of the transfers created by the user, grouped by (any) tag. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **tags** | [**List&lt;long&gt;**](long.md) | The tags to be included in the results.  | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightGroupEntry&gt;**](InsightGroupEntry.md)

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
| **200** | A list of tag and transfer details. Each tag has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insighttransfertotal"></a>
# **InsightTransferTotal**
> List&lt;InsightTotalEntry&gt; InsightTransferTotal (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into total transfers.

This endpoint gives a sum of the total amount transfers made by the user. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTotalEntry&gt;**](InsightTotalEntry.md)

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
| **200** | A list of sums in different currencies. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="insighttransfers"></a>
# **InsightTransfers**
> List&lt;InsightTransferEntry&gt; InsightTransfers (DateOnly start, DateOnly end, Guid xTraceId = null, List<long> accounts = null)

Insight into transfers, grouped by account.

This endpoint gives a summary of the transfers made by the user, grouped by asset account or lability. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **start** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD.  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **accounts** | [**List&lt;long&gt;**](long.md) | The accounts to be included in the results. If you include ID&#39;s of asset accounts or liabilities, only transfers between those asset accounts / liabilities will be included. Other account ID&#39;s will be ignored.  | [optional]  |

### Return type

[**List&lt;InsightTransferEntry&gt;**](InsightTransferEntry.md)

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
| **200** | A list of asset accounts and transfer details. Each asset account has one row per currency. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

