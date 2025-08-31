# Brotal.FireflyIII.Api.AboutApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAbout**](AboutApi.md#getabout) | **GET** /v1/about | System information end point. |
| [**GetCron**](AboutApi.md#getcron) | **GET** /v1/cron/{cliToken} | Cron job endpoint |
| [**GetCurrentUser**](AboutApi.md#getcurrentuser) | **GET** /v1/about/user | Currently authenticated user endpoint. |

<a id="getabout"></a>
# **GetAbout**
> SystemInfo GetAbout (Guid xTraceId = null)

System information end point.

Returns general system information and versions of the (supporting) software. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**SystemInfo**](SystemInfo.md)

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
| **200** | The available system information |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcron"></a>
# **GetCron**
> CronResult GetCron (string cliToken, Guid xTraceId = null, DateOnly date = null, bool force = null)

Cron job endpoint

Firefly III has one endpoint for its various cron related tasks. Send a GET to this endpoint to run the cron. The cron requires the CLI token to be present. The cron job will fire for all users. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **cliToken** | **string** | The CLI token of any user in Firefly III, required to run the cron job. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **date** | **DateOnly** | A date formatted YYYY-MM-DD. This can be used to make the cron job pretend it&#39;s running on another day.  | [optional]  |
| **force** | **bool** | Forces the cron job to fire, regardless of whether it has fired before. This may result in double transactions or weird budgets, so be careful.  | [optional]  |

### Return type

[**CronResult**](CronResult.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The result of the cron job(s) firing. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getcurrentuser"></a>
# **GetCurrentUser**
> UserSingle GetCurrentUser (Guid xTraceId = null)

Currently authenticated user endpoint.

Returns the currently authenticated user. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**UserSingle**](UserSingle.md)

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
| **200** | The user |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

