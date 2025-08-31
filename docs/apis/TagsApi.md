# Brotal.FireflyIII.Api.TagsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteTag**](TagsApi.md#deletetag) | **DELETE** /v1/tags/{tag} | Delete an tag. |
| [**GetTag**](TagsApi.md#gettag) | **GET** /v1/tags/{tag} | Get a single tag. |
| [**ListAttachmentByTag**](TagsApi.md#listattachmentbytag) | **GET** /v1/tags/{tag}/attachments | Lists all attachments. |
| [**ListTag**](TagsApi.md#listtag) | **GET** /v1/tags | List all tags. |
| [**ListTransactionByTag**](TagsApi.md#listtransactionbytag) | **GET** /v1/tags/{tag}/transactions | List all transactions with this tag. |
| [**StoreTag**](TagsApi.md#storetag) | **POST** /v1/tags | Store a new tag |
| [**UpdateTag**](TagsApi.md#updatetag) | **PUT** /v1/tags/{tag} | Update existing tag. |

<a id="deletetag"></a>
# **DeleteTag**
> void DeleteTag (string tag, Guid xTraceId = null)

Delete an tag.

Delete an tag.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tag** | **string** | Either the tag itself or the tag ID. If you use the tag itself, and it contains international (non-ASCII) characters, your mileage may vary. |  |
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
| **204** | Tag deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettag"></a>
# **GetTag**
> TagSingle GetTag (string tag, Guid xTraceId = null, int limit = null, int page = null)

Get a single tag.

Get a single tag.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tag** | **string** | Either the tag itself or the tag ID. If you use the tag itself, and it contains international (non-ASCII) characters, your mileage may vary. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**TagSingle**](TagSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The requested tag |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listattachmentbytag"></a>
# **ListAttachmentByTag**
> AttachmentArray ListAttachmentByTag (string tag, Guid xTraceId = null, int limit = null, int page = null)

Lists all attachments.

Lists all attachments.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tag** | **string** | Either the tag itself or the tag ID. |  |
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
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listtag"></a>
# **ListTag**
> TagArray ListTag (Guid xTraceId = null, int limit = null, int page = null)

List all tags.

List all of the user's tags.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**TagArray**](TagArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of tags |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listtransactionbytag"></a>
# **ListTransactionByTag**
> TransactionArray ListTransactionByTag (string tag, Guid xTraceId = null, int limit = null, int page = null, DateOnly start = null, DateOnly end = null, TransactionTypeFilter type = null)

List all transactions with this tag.

List all transactions with this tag.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tag** | **string** | Either the tag itself or the tag ID. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |
| **start** | **DateOnly** | A date formatted YYYY-MM-DD. This is the start date of the selected range (inclusive).  | [optional]  |
| **end** | **DateOnly** | A date formatted YYYY-MM-DD. This is the end date of the selected range (inclusive).  | [optional]  |
| **type** | **TransactionTypeFilter** | Optional filter on the transaction type(s) returned. | [optional]  |

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

<a id="storetag"></a>
# **StoreTag**
> TagSingle StoreTag (TagModelStore tagModelStore, Guid xTraceId = null)

Store a new tag

Creates a new tag. The data required can be submitted as a JSON body or as a list of parameters.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tagModelStore** | [**TagModelStore**](TagModelStore.md) | JSON array or key&#x3D;value pairs with the necessary tag information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**TagSingle**](TagSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New tag stored, result in response. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatetag"></a>
# **UpdateTag**
> TagSingle UpdateTag (string tag, TagModelUpdate tagModelUpdate, Guid xTraceId = null)

Update existing tag.

Update existing tag.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tag** | **string** | Either the tag itself or the tag ID. If you use the tag itself, and it contains international (non-ASCII) characters, your mileage may vary. |  |
| **tagModelUpdate** | [**TagModelUpdate**](TagModelUpdate.md) | JSON array with updated tag information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**TagSingle**](TagSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated tag stored, result in response |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

