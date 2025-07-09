# OpenAPI\Client\CallRecordingApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDRecordingGet()**](CallRecordingApi.md#v1AccountAccountIDRecordingGet) | **GET** /v1/account/{accountID}/recording | Get Account Call Recording |
| [**v1AccountAccountIDRecordingRecordingIDDelete()**](CallRecordingApi.md#v1AccountAccountIDRecordingRecordingIDDelete) | **DELETE** /v1/account/{accountID}/recording/{recordingID} | Delete Call Recording |
| [**v1AccountAccountIDRecordingRecordingIDGet()**](CallRecordingApi.md#v1AccountAccountIDRecordingRecordingIDGet) | **GET** /v1/account/{accountID}/recording/{recordingID} | Get Call Recording Details |
| [**v1AccountAccountIDUserUserIDRecordingGet()**](CallRecordingApi.md#v1AccountAccountIDUserUserIDRecordingGet) | **GET** /v1/account/{accountID}/user/{userID}/recording | Get User Call Recording |


## `v1AccountAccountIDRecordingGet()`

```php
v1AccountAccountIDRecordingGet($account_id): \OpenAPI\Client\Model\ServiceDocsCallRecordingGetAll
```

Get Account Call Recording

Obtain a list of the call recordings within an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallRecordingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDRecordingGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallRecordingApi->v1AccountAccountIDRecordingGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallRecordingGetAll**](../Model/ServiceDocsCallRecordingGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDRecordingRecordingIDDelete()`

```php
v1AccountAccountIDRecordingRecordingIDDelete($account_id, $recording_id): \OpenAPI\Client\Model\ServiceDocsCallRecordingGetSingle
```

Delete Call Recording

Delete a single call recording from an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallRecordingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$recording_id = 'recording_id_example'; // string | Recording ID, 39 (yyyymm-<32 id>)

try {
    $result = $apiInstance->v1AccountAccountIDRecordingRecordingIDDelete($account_id, $recording_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallRecordingApi->v1AccountAccountIDRecordingRecordingIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **recording_id** | **string**| Recording ID, 39 (yyyymm-&lt;32 id&gt;) | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallRecordingGetSingle**](../Model/ServiceDocsCallRecordingGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDRecordingRecordingIDGet()`

```php
v1AccountAccountIDRecordingRecordingIDGet($account_id, $recording_id): \OpenAPI\Client\Model\ServiceDocsCallRecordingGetSingle
```

Get Call Recording Details

Access details for each recorded call in an account (e.g., duration, names and numbers of call participants, etc.).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallRecordingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$recording_id = 'recording_id_example'; // string | Recording ID, 39 (yyyymm-<32 id>)

try {
    $result = $apiInstance->v1AccountAccountIDRecordingRecordingIDGet($account_id, $recording_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallRecordingApi->v1AccountAccountIDRecordingRecordingIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **recording_id** | **string**| Recording ID, 39 (yyyymm-&lt;32 id&gt;) | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallRecordingGetSingle**](../Model/ServiceDocsCallRecordingGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `audio/mp3`, `audio/mpeg`, `audio/mpeg3`, `audio/x-wav`, `audio/wav`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDUserUserIDRecordingGet()`

```php
v1AccountAccountIDUserUserIDRecordingGet($account_id, $user_id): \OpenAPI\Client\Model\ServiceDocsCallRecordingGetAll
```

Get User Call Recording

Retrieve a list of call recordings for a user within an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallRecordingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$user_id = 'user_id_example'; // string | User ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDUserUserIDRecordingGet($account_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallRecordingApi->v1AccountAccountIDUserUserIDRecordingGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **user_id** | **string**| User ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallRecordingGetAll**](../Model/ServiceDocsCallRecordingGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
