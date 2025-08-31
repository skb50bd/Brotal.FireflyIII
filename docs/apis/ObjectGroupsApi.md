# Brotal.FireflyIII.Api.ObjectGroupsApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteObjectGroup**](ObjectGroupsApi.md#deleteobjectgroup) | **DELETE** /v1/object-groups/{id} | Delete a object group. |
| [**GetObjectGroup**](ObjectGroupsApi.md#getobjectgroup) | **GET** /v1/object-groups/{id} | Get a single object group. |
| [**ListBillByObjectGroup**](ObjectGroupsApi.md#listbillbyobjectgroup) | **GET** /v1/object-groups/{id}/bills | List all bills with this object group. |
| [**ListObjectGroups**](ObjectGroupsApi.md#listobjectgroups) | **GET** /v1/object-groups | List all object groups. |
| [**ListPiggyBankByObjectGroup**](ObjectGroupsApi.md#listpiggybankbyobjectgroup) | **GET** /v1/object-groups/{id}/piggy-banks | List all piggy banks related to the object group. |
| [**UpdateObjectGroup**](ObjectGroupsApi.md#updateobjectgroup) | **PUT** /v1/object-groups/{id} | Update existing object group. |

<a id="deleteobjectgroup"></a>
# **DeleteObjectGroup**
> void DeleteObjectGroup (string id, Guid xTraceId = null)

Delete a object group.

Delete a object group.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the object group. |  |
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
| **204** | Object group deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getobjectgroup"></a>
# **GetObjectGroup**
> ObjectGroupSingle GetObjectGroup (string id, Guid xTraceId = null)

Get a single object group.

Get a single object group.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the object group. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**ObjectGroupSingle**](ObjectGroupSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The requested object group |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listbillbyobjectgroup"></a>
# **ListBillByObjectGroup**
> BillArray ListBillByObjectGroup (string id, Guid xTraceId = null, int limit = null, int page = null)

List all bills with this object group.

List all bills with this object group.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the account. |  |
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

<a id="listobjectgroups"></a>
# **ListObjectGroups**
> ObjectGroupArray ListObjectGroups (Guid xTraceId = null, int limit = null, int page = null)

List all object groups.

List all object groups.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**ObjectGroupArray**](ObjectGroupArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of object groups |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listpiggybankbyobjectgroup"></a>
# **ListPiggyBankByObjectGroup**
> PiggyBankArray ListPiggyBankByObjectGroup (string id, Guid xTraceId = null, int limit = null, int page = null)

List all piggy banks related to the object group.

This endpoint returns a list of all the piggy banks connected to the object group. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the account. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**PiggyBankArray**](PiggyBankArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of piggy banks |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateobjectgroup"></a>
# **UpdateObjectGroup**
> ObjectGroupSingle UpdateObjectGroup (string id, ObjectGroupUpdate objectGroupUpdate, Guid xTraceId = null)

Update existing object group.

Update existing object group.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The ID of the object group |  |
| **objectGroupUpdate** | [**ObjectGroupUpdate**](ObjectGroupUpdate.md) | JSON array with updated piggy bank information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**ObjectGroupSingle**](ObjectGroupSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated object group stored, result in response |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

