# Brotal.FireflyIII.Api.WebhooksApi

All URIs are relative to *https://demo.firefly-iii.org/api*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteWebhook**](WebhooksApi.md#deletewebhook) | **DELETE** /v1/webhooks/{id} | Delete a webhook. |
| [**DeleteWebhookMessage**](WebhooksApi.md#deletewebhookmessage) | **DELETE** /v1/webhooks/{id}/messages/{messageId} | Delete a webhook message. |
| [**DeleteWebhookMessageAttempt**](WebhooksApi.md#deletewebhookmessageattempt) | **DELETE** /v1/webhooks/{id}/messages/{messageId}/attempts/{attemptId} | Delete a webhook attempt. |
| [**GetSingleWebhookMessage**](WebhooksApi.md#getsinglewebhookmessage) | **GET** /v1/webhooks/{id}/messages/{messageId} | Get a single message from a webhook. |
| [**GetSingleWebhookMessageAttempt**](WebhooksApi.md#getsinglewebhookmessageattempt) | **GET** /v1/webhooks/{id}/messages/{messageId}/attempts/{attemptId} | Get a single failed attempt from a single webhook message. |
| [**GetWebhook**](WebhooksApi.md#getwebhook) | **GET** /v1/webhooks/{id} | Get a single webhook. |
| [**GetWebhookMessageAttempts**](WebhooksApi.md#getwebhookmessageattempts) | **GET** /v1/webhooks/{id}/messages/{messageId}/attempts | Get all the failed attempts of a single webhook message. |
| [**GetWebhookMessages**](WebhooksApi.md#getwebhookmessages) | **GET** /v1/webhooks/{id}/messages | Get all the messages of a single webhook. |
| [**ListWebhook**](WebhooksApi.md#listwebhook) | **GET** /v1/webhooks | List all webhooks. |
| [**StoreWebhook**](WebhooksApi.md#storewebhook) | **POST** /v1/webhooks | Store a new webhook |
| [**SubmitWebhook**](WebhooksApi.md#submitwebhook) | **POST** /v1/webhooks/{id}/submit | Submit messages for a webhook. |
| [**TriggerTransactionWebhook**](WebhooksApi.md#triggertransactionwebhook) | **POST** /v1/webhooks/{id}/trigger-transaction/{transactionId} | Trigger webhook for a given transaction. |
| [**UpdateWebhook**](WebhooksApi.md#updatewebhook) | **PUT** /v1/webhooks/{id} | Update existing webhook. |

<a id="deletewebhook"></a>
# **DeleteWebhook**
> void DeleteWebhook (string id, Guid xTraceId = null)

Delete a webhook.

Delete a webhook.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
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
| **204** | Webhook deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletewebhookmessage"></a>
# **DeleteWebhookMessage**
> void DeleteWebhookMessage (string id, int messageId, Guid xTraceId = null)

Delete a webhook message.

Delete a webhook message. Any time a webhook is triggered the message is stored before it's sent. You can delete them before or after sending.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **messageId** | **int** | The webhook message ID. |  |
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
| **204** | Webhook message deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletewebhookmessageattempt"></a>
# **DeleteWebhookMessageAttempt**
> void DeleteWebhookMessageAttempt (string id, int messageId, int attemptId, Guid xTraceId = null)

Delete a webhook attempt.

Delete a webhook message attempt. If you delete all attempts for a webhook message, Firefly III will (once again) assume all is well with the webhook message and will try to send it again.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **messageId** | **int** | The webhook message ID. |  |
| **attemptId** | **int** | The webhook message attempt ID. |  |
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
| **204** | Webhook message attempt deleted. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getsinglewebhookmessage"></a>
# **GetSingleWebhookMessage**
> WebhookMessageSingle GetSingleWebhookMessage (string id, int messageId, Guid xTraceId = null)

Get a single message from a webhook.

When a webhook is triggered it will store the actual content of the webhook in a webhook message. You can view and analyse a single one using this endpoint.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **messageId** | **int** | The webhook message ID. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**WebhookMessageSingle**](WebhookMessageSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A single webhook message. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getsinglewebhookmessageattempt"></a>
# **GetSingleWebhookMessageAttempt**
> WebhookAttemptSingle GetSingleWebhookMessageAttempt (string id, int messageId, int attemptId, Guid xTraceId = null)

Get a single failed attempt from a single webhook message.

When a webhook message fails to send it will store the failure in an \"attempt\". You can view and analyse these. Webhooks messages that receive too many attempts (failures) will not be fired. You must first clear out old attempts and try again. This endpoint shows you the details of a single attempt. The ID of the attempt must match the corresponding webhook and webhook message.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **messageId** | **int** | The webhook message ID. |  |
| **attemptId** | **int** | The webhook attempt ID. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**WebhookAttemptSingle**](WebhookAttemptSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A single webhook attempt. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getwebhook"></a>
# **GetWebhook**
> WebhookSingle GetWebhook (string id, Guid xTraceId = null)

Get a single webhook.

Gets all info of a single webhook.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**WebhookSingle**](WebhookSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The requested webhook. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getwebhookmessageattempts"></a>
# **GetWebhookMessageAttempts**
> WebhookAttemptArray GetWebhookMessageAttempts (string id, int messageId, Guid xTraceId = null, int limit = null, int page = null)

Get all the failed attempts of a single webhook message.

When a webhook message fails to send it will store the failure in an \"attempt\". You can view and analyse these. Webhook messages that receive too many attempts (failures) will not be sent again. You must first clear out old attempts before the message can go out again.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **messageId** | **int** | The webhook message ID. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**WebhookAttemptArray**](WebhookAttemptArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of webhook attempts. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getwebhookmessages"></a>
# **GetWebhookMessages**
> WebhookMessageArray GetWebhookMessages (string id, Guid xTraceId = null)

Get all the messages of a single webhook.

When a webhook is triggered the actual message that will be send is stored in a \"message\". You can view and analyse these messages.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**WebhookMessageArray**](WebhookMessageArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of webhook messages. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="listwebhook"></a>
# **ListWebhook**
> WebhookArray ListWebhook (Guid xTraceId = null, int limit = null, int page = null)

List all webhooks.

List all the user's webhooks.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |
| **limit** | **int** | Number of items per page. The default pagination is per 50 items. | [optional]  |
| **page** | **int** | Page number. The default pagination is per 50 items. | [optional]  |

### Return type

[**WebhookArray**](WebhookArray.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A list of webhooks. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="storewebhook"></a>
# **StoreWebhook**
> WebhookSingle StoreWebhook (WebhookStore webhookStore, Guid xTraceId = null)

Store a new webhook

Creates a new webhook. The data required can be submitted as a JSON body or as a list of parameters. The webhook will be given a random secret. 


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookStore** | [**WebhookStore**](WebhookStore.md) | JSON array or key&#x3D;value pairs with the necessary webhook information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**WebhookSingle**](WebhookSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | New webhook stored, result in response. |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="submitwebhook"></a>
# **SubmitWebhook**
> void SubmitWebhook (string id, Guid xTraceId = null)

Submit messages for a webhook.

This endpoint will submit any open messages for this webhook. This is an asynchronous operation, so you can't see the result. Refresh the webhook message and/or the webhook message attempts to see the results. This may take some time if the webhook receiver is slow.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
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
| **400** | Bad request |  -  |
| **200** | OK. |  -  |
| **204** | No messages to send, so did nothing. |  -  |
| **404** | Page not found |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="triggertransactionwebhook"></a>
# **TriggerTransactionWebhook**
> void TriggerTransactionWebhook (string id, string transactionId, Guid xTraceId = null)

Trigger webhook for a given transaction.

This endpoint will execute this webhook for a given transaction ID. This is an asynchronous operation, so you can't see the result. Refresh the webhook message and/or the webhook message attempts to see the results. This may take some time if the webhook receiver is slow.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **transactionId** | **string** | The transaction ID. |  |
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
| **400** | Bad request |  -  |
| **204** | Webhook triggered successfully. |  -  |
| **404** | Page not found |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatewebhook"></a>
# **UpdateWebhook**
> WebhookSingle UpdateWebhook (string id, WebhookUpdate webhookUpdate, Guid xTraceId = null)

Update existing webhook.

Update an existing webhook's information. If you wish to reset the secret, submit any value as the \"secret\". Firefly III will take this as a hint and reset the secret of the webhook.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **string** | The webhook ID. |  |
| **webhookUpdate** | [**WebhookUpdate**](WebhookUpdate.md) | JSON array with updated webhook information. See the model for the exact specifications. |  |
| **xTraceId** | **Guid** | Unique identifier associated with this request. | [optional]  |

### Return type

[**WebhookSingle**](WebhookSingle.md)

### Authorization

[firefly_iii_auth](../README.md#firefly_iii_auth), [local_bearer_auth](../README.md#local_bearer_auth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/vnd.api+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated webhook stored, result in response |  -  |
| **422** | Validation error. The body will have the exact details. |  -  |
| **401** | Unauthenticated |  -  |
| **404** | Page not found |  -  |
| **400** | Bad request |  -  |
| **500** | Internal exception |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

