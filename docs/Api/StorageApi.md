# OpenAPI\Client\StorageApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDStorageDelete()**](StorageApi.md#v1AccountAccountIDStorageDelete) | **DELETE** /v1/account/{accountID}/storage | Delete Storage |
| [**v1AccountAccountIDStorageGet()**](StorageApi.md#v1AccountAccountIDStorageGet) | **GET** /v1/account/{accountID}/storage | Get Storage Details |
| [**v1AccountAccountIDStoragePost()**](StorageApi.md#v1AccountAccountIDStoragePost) | **POST** /v1/account/{accountID}/storage | Create Storage |
| [**v1AccountAccountIDStoragePut()**](StorageApi.md#v1AccountAccountIDStoragePut) | **PUT** /v1/account/{accountID}/storage | Update Storage |


## `v1AccountAccountIDStorageDelete()`

```php
v1AccountAccountIDStorageDelete($account_id): \OpenAPI\Client\Model\ServiceDocsStorageGet
```

Delete Storage

Delete items that are stored in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\StorageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDStorageDelete($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorageApi->v1AccountAccountIDStorageDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsStorageGet**](../Model/ServiceDocsStorageGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDStorageGet()`

```php
v1AccountAccountIDStorageGet($account_id): \OpenAPI\Client\Model\ServiceDocsStorageGet
```

Get Storage Details

Retrieve storage details for an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\StorageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDStorageGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorageApi->v1AccountAccountIDStorageGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsStorageGet**](../Model/ServiceDocsStorageGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDStoragePost()`

```php
v1AccountAccountIDStoragePost($account_id, $req_body): \OpenAPI\Client\Model\ServiceDocsStorageGet
```

Create Storage

Create storage in an account for voicemails, call recordings, faxes, etc.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\StorageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPStorageAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPStorageAddEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDStoragePost($account_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorageApi->v1AccountAccountIDStoragePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPStorageAddEditData**](../Model/ServiceVOIPStorageAddEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsStorageGet**](../Model/ServiceDocsStorageGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDStoragePut()`

```php
v1AccountAccountIDStoragePut($account_id, $req_body): \OpenAPI\Client\Model\ServiceDocsStorageGet
```

Update Storage

Modify the names of metadata to make it easier to locate (e.g., change the name of voicemail_storage to voicemail_and_callrecordings_storage, etc.).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\StorageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPStorageAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPStorageAddEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDStoragePut($account_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorageApi->v1AccountAccountIDStoragePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPStorageAddEditData**](../Model/ServiceVOIPStorageAddEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsStorageGet**](../Model/ServiceDocsStorageGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
