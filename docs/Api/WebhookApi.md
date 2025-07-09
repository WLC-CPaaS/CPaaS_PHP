# OpenAPI\Client\WebhookApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1WebhookAccountAccountIDGet()**](WebhookApi.md#v1WebhookAccountAccountIDGet) | **GET** /v1/webhook/account/{accountID} | Get Webhook List |
| [**v1WebhookAccountAccountIDPost()**](WebhookApi.md#v1WebhookAccountAccountIDPost) | **POST** /v1/webhook/account/{accountID} | Create Webhook |
| [**v1WebhookAccountAccountIDWebhookIDDelete()**](WebhookApi.md#v1WebhookAccountAccountIDWebhookIDDelete) | **DELETE** /v1/webhook/account/{accountID}/{webhookID} | Delete Webhook |
| [**v1WebhookAccountAccountIDWebhookIDGet()**](WebhookApi.md#v1WebhookAccountAccountIDWebhookIDGet) | **GET** /v1/webhook/account/{accountID}/{webhookID} | Get Webhook Details |
| [**v1WebhookAccountAccountIDWebhookIDPut()**](WebhookApi.md#v1WebhookAccountAccountIDWebhookIDPut) | **PUT** /v1/webhook/account/{accountID}/{webhookID} | Update Webhook |


## `v1WebhookAccountAccountIDGet()`

```php
v1WebhookAccountAccountIDGet($account_id, $page_size, $current_page): \OpenAPI\Client\Model\ServiceDocsWebhookGetAll
```

Get Webhook List

Retrieve the webhook list in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID
$page_size = 56; // int | number of records to return, range 1 to 50
$current_page = 56; // int | Current Page

try {
    $result = $apiInstance->v1WebhookAccountAccountIDGet($account_id, $page_size, $current_page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->v1WebhookAccountAccountIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID | |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |
| **current_page** | **int**| Current Page | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsWebhookGetAll**](../Model/ServiceDocsWebhookGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1WebhookAccountAccountIDPost()`

```php
v1WebhookAccountAccountIDPost($account_id, $body): \OpenAPI\Client\Model\ServiceDocsWebhookGetSingle
```

Create Webhook

Create a webhook for a specific account ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID
$body = new \OpenAPI\Client\Model\ServiceWebhookAdd(); // \OpenAPI\Client\Model\ServiceWebhookAdd | Webhook data

try {
    $result = $apiInstance->v1WebhookAccountAccountIDPost($account_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->v1WebhookAccountAccountIDPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID | |
| **body** | [**\OpenAPI\Client\Model\ServiceWebhookAdd**](../Model/ServiceWebhookAdd.md)| Webhook data | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsWebhookGetSingle**](../Model/ServiceDocsWebhookGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1WebhookAccountAccountIDWebhookIDDelete()`

```php
v1WebhookAccountAccountIDWebhookIDDelete($account_id, $webhook_id): \OpenAPI\Client\Model\ServiceDocsWebhookDelete
```

Delete Webhook

Remove a webhook identified by its ID for a particular account ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID
$webhook_id = 56; // int | Webhook ID

try {
    $result = $apiInstance->v1WebhookAccountAccountIDWebhookIDDelete($account_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->v1WebhookAccountAccountIDWebhookIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID | |
| **webhook_id** | **int**| Webhook ID | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsWebhookDelete**](../Model/ServiceDocsWebhookDelete.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1WebhookAccountAccountIDWebhookIDGet()`

```php
v1WebhookAccountAccountIDWebhookIDGet($account_id, $webhook_id): \OpenAPI\Client\Model\ServiceDocsWebhookGetSingle
```

Get Webhook Details

Access details about a single webhook ID for an individual account ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID
$webhook_id = 56; // int | Webhook ID

try {
    $result = $apiInstance->v1WebhookAccountAccountIDWebhookIDGet($account_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->v1WebhookAccountAccountIDWebhookIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID | |
| **webhook_id** | **int**| Webhook ID | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsWebhookGetSingle**](../Model/ServiceDocsWebhookGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1WebhookAccountAccountIDWebhookIDPut()`

```php
v1WebhookAccountAccountIDWebhookIDPut($account_id, $webhook_id, $body): \OpenAPI\Client\Model\ServiceDocsWebhookGetSingle
```

Update Webhook

Update a webhook identified by its ID for a distinct account ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID
$webhook_id = 'webhook_id_example'; // string | Webhook ID
$body = new \OpenAPI\Client\Model\ServiceWebhookEdit(); // \OpenAPI\Client\Model\ServiceWebhookEdit | Updated webhook data

try {
    $result = $apiInstance->v1WebhookAccountAccountIDWebhookIDPut($account_id, $webhook_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->v1WebhookAccountAccountIDWebhookIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID | |
| **webhook_id** | **string**| Webhook ID | |
| **body** | [**\OpenAPI\Client\Model\ServiceWebhookEdit**](../Model/ServiceWebhookEdit.md)| Updated webhook data | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsWebhookGetSingle**](../Model/ServiceDocsWebhookGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
