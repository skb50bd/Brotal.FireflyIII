# Brotal.FireflyIII.Api.ConfigurationApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetConfiguration**](ConfigurationApi.md#getconfiguration) | **GET** /v1/configuration | Get Firefly III system configuration values. |
| [**GetSingleConfiguration**](ConfigurationApi.md#getsingleconfiguration) | **GET** /v1/configuration/{name} | Get a single Firefly III system configuration value |
| [**SetConfiguration**](ConfigurationApi.md#setconfiguration) | **PUT** /v1/configuration/{name} | Update configuration value |

<a id="getconfiguration"></a>
# **GetConfiguration**
> List&lt;ModelConfiguration&gt; GetConfiguration (Guid xTraceId = null)

Get Firefly III system configuration values.

Returns all editable and not-editable configuration values for this Firefly III installation


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**List&lt;ModelConfiguration&gt;**](ModelConfiguration.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/x-www-form-urlencoded


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |
| **200** | System configuration values |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getsingleconfiguration"></a>
# **GetSingleConfiguration**
> ConfigurationSingle GetSingleConfiguration (ConfigValueFilter name, Guid xTraceId = null)

Get a single Firefly III system configuration value

Returns one configuration variable for this Firefly III installation


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **name** | **ConfigValueFilter** | The name of the configuration value you want to know. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**ConfigurationSingle**](ConfigurationSingle.md)

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
| **200** | One system configuration value |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setconfiguration"></a>
# **SetConfiguration**
> ConfigurationSingle SetConfiguration (ConfigValueUpdateFilter name, PolymorphicProperty value, Guid xTraceId = null)

Update configuration value

Set a single configuration value. Not all configuration values can be updated so the list of accepted configuration variables is small.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **name** | **ConfigValueUpdateFilter** | The name of the configuration value you want to update. |  |
| **value** | [**PolymorphicProperty**](PolymorphicProperty.md) |  |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**ConfigurationSingle**](ConfigurationSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded, application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New configuration value stored, result in response. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

