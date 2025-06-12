# OpenAPI\Client\PresenceApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDPresenceExtensionPut()**](PresenceApi.md#v1AccountAccountIDPresenceExtensionPut) | **PUT** /v1/account/{accountID}/presence/{extension} | Set/Reset Presence for Extension |
| [**v1AccountAccountIDPresenceGet()**](PresenceApi.md#v1AccountAccountIDPresenceGet) | **GET** /v1/account/{accountID}/presence | Get Presence Details |
| [**v1AccountAccountIDUserUserIDPresencePut()**](PresenceApi.md#v1AccountAccountIDUserUserIDPresencePut) | **PUT** /v1/account/{accountID}/user/{userID}/presence | Set/Reset Presence for User |


## `v1AccountAccountIDPresenceExtensionPut()`

```php
v1AccountAccountIDPresenceExtensionPut($account_id, $extension, $req_body): \OpenAPI\Client\Model\ServiceAPIResponse
```

Set/Reset Presence for Extension

Set or reset the presence status of an extension.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PresenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$extension = 'extension_example'; // string | Extension
$req_body = new \OpenAPI\Client\Model\ServiceVOIPPresenceSetResetEditData(); // \OpenAPI\Client\Model\ServiceVOIPPresenceSetResetEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDPresenceExtensionPut($account_id, $extension, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PresenceApi->v1AccountAccountIDPresenceExtensionPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **extension** | **string**| Extension | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPPresenceSetResetEditData**](../Model/ServiceVOIPPresenceSetResetEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceAPIResponse**](../Model/ServiceAPIResponse.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDPresenceGet()`

```php
v1AccountAccountIDPresenceGet($account_id): \OpenAPI\Client\Model\ServiceDocsPresenceGet
```

Get Presence Details

Retrieve details of presence subscriptions in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PresenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDPresenceGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PresenceApi->v1AccountAccountIDPresenceGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsPresenceGet**](../Model/ServiceDocsPresenceGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDUserUserIDPresencePut()`

```php
v1AccountAccountIDUserUserIDPresencePut($account_id, $user_id, $req_body): \OpenAPI\Client\Model\ServiceAPIResponse
```

Set/Reset Presence for User

Set or reset the presence status of a user within an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PresenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$user_id = 'user_id_example'; // string | User ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPPresenceSetResetEditData(); // \OpenAPI\Client\Model\ServiceVOIPPresenceSetResetEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDUserUserIDPresencePut($account_id, $user_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PresenceApi->v1AccountAccountIDUserUserIDPresencePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **user_id** | **string**| User ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPPresenceSetResetEditData**](../Model/ServiceVOIPPresenceSetResetEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceAPIResponse**](../Model/ServiceAPIResponse.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
