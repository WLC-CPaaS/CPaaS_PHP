# OpenAPI\Client\MediaApi

All URIs are relative to http://api.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDMediaMediaIDFileGet()**](MediaApi.md#v1AccountAccountIDMediaMediaIDFileGet) | **GET** /v1/account/{accountID}/media/{mediaID}/file | Get Media File |
| [**v1AccountAccountIDMediaMediaIDFilePost()**](MediaApi.md#v1AccountAccountIDMediaMediaIDFilePost) | **POST** /v1/account/{accountID}/media/{mediaID}/file | Add Media File |
| [**v1AccountAccountidMediaGet()**](MediaApi.md#v1AccountAccountidMediaGet) | **GET** /v1/account/{accountid}/media | Get Media List |
| [**v1AccountAccountidMediaMediaidDelete()**](MediaApi.md#v1AccountAccountidMediaMediaidDelete) | **DELETE** /v1/account/{accountid}/media/{mediaid} | Delete Media |
| [**v1AccountAccountidMediaMediaidGet()**](MediaApi.md#v1AccountAccountidMediaMediaidGet) | **GET** /v1/account/{accountid}/media/{mediaid} | Get Media Details |
| [**v1AccountAccountidMediaPost()**](MediaApi.md#v1AccountAccountidMediaPost) | **POST** /v1/account/{accountid}/media | Create Media |


## `v1AccountAccountIDMediaMediaIDFileGet()`

```php
v1AccountAccountIDMediaMediaIDFileGet($account_id, $media_id): \SplFileObject
```

Get Media File

Gather data about the media objects in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$media_id = 'media_id_example'; // string | Media ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDMediaMediaIDFileGet($account_id, $media_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->v1AccountAccountIDMediaMediaIDFileGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **media_id** | **string**| Media ID, 32 alpha numeric | |

### Return type

**\SplFileObject**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `audio/mp3`, `audio/mpeg`, `audio/mpeg3`, `audio/x-wav`, `audio/wav`, `audio/ogg`, `video/x-flv`, `video/h264`, `video/mpeg`, `video/quicktime`, `video/mp4`, `video/webm`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDMediaMediaIDFilePost()`

```php
v1AccountAccountIDMediaMediaIDFilePost($account_id, $media_id, $file): \OpenAPI\Client\Model\ServiceDocsMediaGetSingle
```

Add Media File

Include a media file that is connected to a media object in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$media_id = 'media_id_example'; // string | Media ID, 32 alpha numeric
$file = '/path/to/file.txt'; // \SplFileObject | Media file

try {
    $result = $apiInstance->v1AccountAccountIDMediaMediaIDFilePost($account_id, $media_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->v1AccountAccountIDMediaMediaIDFilePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **media_id** | **string**| Media ID, 32 alpha numeric | |
| **file** | **\SplFileObject****\SplFileObject**| Media file | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMediaGetSingle**](../Model/ServiceDocsMediaGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidMediaGet()`

```php
v1AccountAccountidMediaGet($accountid, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsMediaGetAll
```

Get Media List

View all media files for an account in your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountidMediaGet($accountid, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->v1AccountAccountidMediaGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMediaGetAll**](../Model/ServiceDocsMediaGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidMediaMediaidDelete()`

```php
v1AccountAccountidMediaMediaidDelete($accountid, $mediaid): \OpenAPI\Client\Model\ServiceDocsMediaGetSingle
```

Delete Media

Remove a media file that is no longer in use from an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$mediaid = 'mediaid_example'; // string | Device ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidMediaMediaidDelete($accountid, $mediaid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->v1AccountAccountidMediaMediaidDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **mediaid** | **string**| Device ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMediaGetSingle**](../Model/ServiceDocsMediaGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidMediaMediaidGet()`

```php
v1AccountAccountidMediaMediaidGet($accountid, $mediaid): \OpenAPI\Client\Model\ServiceDocsMediaGetSingle
```

Get Media Details

Permit users to view an account's specific media information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$mediaid = 'mediaid_example'; // string | Media ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidMediaMediaidGet($accountid, $mediaid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->v1AccountAccountidMediaMediaidGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **mediaid** | **string**| Media ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMediaGetSingle**](../Model/ServiceDocsMediaGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidMediaPost()`

```php
v1AccountAccountidMediaPost($accountid, $media): \OpenAPI\Client\Model\ServiceDocsMediaGetSingle
```

Create Media

Generate a media object to allow users to upload a media file in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MediaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$media = new \OpenAPI\Client\Model\ServiceVOIPMediaAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPMediaAddEditData | Media creation or update payload

try {
    $result = $apiInstance->v1AccountAccountidMediaPost($accountid, $media);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MediaApi->v1AccountAccountidMediaPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **media** | [**\OpenAPI\Client\Model\ServiceVOIPMediaAddEditData**](../Model/ServiceVOIPMediaAddEditData.md)| Media creation or update payload | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMediaGetSingle**](../Model/ServiceDocsMediaGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
