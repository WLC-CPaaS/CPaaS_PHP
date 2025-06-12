# OpenAPI\Client\ChannelApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDChannelChannelIDGet()**](ChannelApi.md#v1AccountAccountIDChannelChannelIDGet) | **GET** /v1/account/{accountID}/channel/{channelID} | Get Channel Details |
| [**v1AccountAccountIDChannelChannelIDPost()**](ChannelApi.md#v1AccountAccountIDChannelChannelIDPost) | **POST** /v1/account/{accountID}/channel/{channelID} | Associate Action to Channel |
| [**v1AccountAccountIDChannelChannelIDPut()**](ChannelApi.md#v1AccountAccountIDChannelChannelIDPut) | **PUT** /v1/account/{accountID}/channel/{channelID} | Associate Metaflow to Channel |
| [**v1AccountAccountIDChannelGet()**](ChannelApi.md#v1AccountAccountIDChannelGet) | **GET** /v1/account/{accountID}/channel | Get Account Channel List |
| [**v1AccountAccountIDDeviceDeviceIDChannelGet()**](ChannelApi.md#v1AccountAccountIDDeviceDeviceIDChannelGet) | **GET** /v1/account/{accountID}/device/{deviceID}/channel | Get Device Channel List |
| [**v1AccountAccountIDUserUserIDChannelGet()**](ChannelApi.md#v1AccountAccountIDUserUserIDChannelGet) | **GET** /v1/account/{accountID}/user/{userID}/channel | Get User Channel List |


## `v1AccountAccountIDChannelChannelIDGet()`

```php
v1AccountAccountIDChannelChannelIDGet($account_id, $channel_id): \OpenAPI\Client\Model\ServiceDocsChannelGetSingle
```

Get Channel Details

Access details about each channel in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$channel_id = 'channel_id_example'; // string | Channel ID

try {
    $result = $apiInstance->v1AccountAccountIDChannelChannelIDGet($account_id, $channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelApi->v1AccountAccountIDChannelChannelIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **channel_id** | **string**| Channel ID | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsChannelGetSingle**](../Model/ServiceDocsChannelGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDChannelChannelIDPost()`

```php
v1AccountAccountIDChannelChannelIDPost($account_id, $channel_id, $req_body): \OpenAPI\Client\Model\ServiceAPIResponse
```

Associate Action to Channel

Link an action, such as transfer or hangup to a channel.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$channel_id = 'channel_id_example'; // string | Channel ID
$req_body = new \OpenAPI\Client\Model\ServiceVOIPChannelRunActionData(); // \OpenAPI\Client\Model\ServiceVOIPChannelRunActionData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDChannelChannelIDPost($account_id, $channel_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelApi->v1AccountAccountIDChannelChannelIDPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **channel_id** | **string**| Channel ID | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPChannelRunActionData**](../Model/ServiceVOIPChannelRunActionData.md)| payload fields | |

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

## `v1AccountAccountIDChannelChannelIDPut()`

```php
v1AccountAccountIDChannelChannelIDPut($account_id, $channel_id, $req_body): \OpenAPI\Client\Model\ServiceAPIResponse
```

Associate Metaflow to Channel

Link a metaflow to an active channel.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$channel_id = 'channel_id_example'; // string | Channel ID
$req_body = new \OpenAPI\Client\Model\ServiceVOIPChannelRunMetaflowData(); // \OpenAPI\Client\Model\ServiceVOIPChannelRunMetaflowData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDChannelChannelIDPut($account_id, $channel_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelApi->v1AccountAccountIDChannelChannelIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **channel_id** | **string**| Channel ID | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPChannelRunMetaflowData**](../Model/ServiceVOIPChannelRunMetaflowData.md)| payload fields | |

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

## `v1AccountAccountIDChannelGet()`

```php
v1AccountAccountIDChannelGet($account_id): \OpenAPI\Client\Model\ServiceDocsChannelGetAll
```

Get Account Channel List

Get a list of active channels for an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDChannelGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelApi->v1AccountAccountIDChannelGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsChannelGetAll**](../Model/ServiceDocsChannelGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDDeviceDeviceIDChannelGet()`

```php
v1AccountAccountIDDeviceDeviceIDChannelGet($account_id, $device_id): \OpenAPI\Client\Model\ServiceDocsChannelGetAll
```

Get Device Channel List

Get the list of active channels for a device.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$device_id = 'device_id_example'; // string | Device ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDDeviceDeviceIDChannelGet($account_id, $device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelApi->v1AccountAccountIDDeviceDeviceIDChannelGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **device_id** | **string**| Device ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsChannelGetAll**](../Model/ServiceDocsChannelGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDUserUserIDChannelGet()`

```php
v1AccountAccountIDUserUserIDChannelGet($account_id, $user_id): \OpenAPI\Client\Model\ServiceDocsChannelGetAll
```

Get User Channel List

Get the list of active channels for a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$user_id = 'user_id_example'; // string | User ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDUserUserIDChannelGet($account_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelApi->v1AccountAccountIDUserUserIDChannelGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **user_id** | **string**| User ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsChannelGetAll**](../Model/ServiceDocsChannelGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
