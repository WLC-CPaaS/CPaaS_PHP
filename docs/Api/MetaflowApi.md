# OpenAPI\Client\MetaflowApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDDeviceDeviceIDMetaflowDelete()**](MetaflowApi.md#v1AccountAccountIDDeviceDeviceIDMetaflowDelete) | **DELETE** /v1/account/{accountID}/device/{deviceID}/metaflow | Delete Device Metaflow |
| [**v1AccountAccountIDDeviceDeviceIDMetaflowGet()**](MetaflowApi.md#v1AccountAccountIDDeviceDeviceIDMetaflowGet) | **GET** /v1/account/{accountID}/device/{deviceID}/metaflow | Get Device Metaflow List |
| [**v1AccountAccountIDDeviceDeviceIDMetaflowPost()**](MetaflowApi.md#v1AccountAccountIDDeviceDeviceIDMetaflowPost) | **POST** /v1/account/{accountID}/device/{deviceID}/metaflow | Create Device Metaflow |
| [**v1AccountAccountIDMetaflowDelete()**](MetaflowApi.md#v1AccountAccountIDMetaflowDelete) | **DELETE** /v1/account/{accountID}/metaflow | Delete Account Metaflow |
| [**v1AccountAccountIDMetaflowGet()**](MetaflowApi.md#v1AccountAccountIDMetaflowGet) | **GET** /v1/account/{accountID}/metaflow | Get Account Metaflow List |
| [**v1AccountAccountIDMetaflowPost()**](MetaflowApi.md#v1AccountAccountIDMetaflowPost) | **POST** /v1/account/{accountID}/metaflow | Create Account Metaflow |
| [**v1AccountAccountIDUserUserIDMetaflowDelete()**](MetaflowApi.md#v1AccountAccountIDUserUserIDMetaflowDelete) | **DELETE** /v1/account/{accountID}/user/{userID}/metaflow | Delete User Metaflow |
| [**v1AccountAccountIDUserUserIDMetaflowGet()**](MetaflowApi.md#v1AccountAccountIDUserUserIDMetaflowGet) | **GET** /v1/account/{accountID}/user/{userID}/metaflow | Get User Metaflow List |
| [**v1AccountAccountIDUserUserIDMetaflowPost()**](MetaflowApi.md#v1AccountAccountIDUserUserIDMetaflowPost) | **POST** /v1/account/{accountID}/user/{userID}/metaflow | Create User Metaflow |


## `v1AccountAccountIDDeviceDeviceIDMetaflowDelete()`

```php
v1AccountAccountIDDeviceDeviceIDMetaflowDelete($account_id, $device_id): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Delete Device Metaflow

Delete all metaflows associated with a device.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$device_id = 'device_id_example'; // string | Device ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDDeviceDeviceIDMetaflowDelete($account_id, $device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDDeviceDeviceIDMetaflowDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **device_id** | **string**| Device ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDDeviceDeviceIDMetaflowGet()`

```php
v1AccountAccountIDDeviceDeviceIDMetaflowGet($account_id, $device_id): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Get Device Metaflow List

Get the list of metaflows for a device.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$device_id = 'device_id_example'; // string | Device ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDDeviceDeviceIDMetaflowGet($account_id, $device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDDeviceDeviceIDMetaflowGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **device_id** | **string**| Device ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDDeviceDeviceIDMetaflowPost()`

```php
v1AccountAccountIDDeviceDeviceIDMetaflowPost($account_id, $device_id, $req_body): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Create Device Metaflow

Create a metaflow or multiple metaflows for a device.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$device_id = 'device_id_example'; // string | Device ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPMetaflowAddData(); // \OpenAPI\Client\Model\ServiceVOIPMetaflowAddData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDDeviceDeviceIDMetaflowPost($account_id, $device_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDDeviceDeviceIDMetaflowPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **device_id** | **string**| Device ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPMetaflowAddData**](../Model/ServiceVOIPMetaflowAddData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDMetaflowDelete()`

```php
v1AccountAccountIDMetaflowDelete($account_id): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Delete Account Metaflow

Remove all metaflows from an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDMetaflowDelete($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDMetaflowDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDMetaflowGet()`

```php
v1AccountAccountIDMetaflowGet($account_id): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Get Account Metaflow List

Get an account's metaflow list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDMetaflowGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDMetaflowGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDMetaflowPost()`

```php
v1AccountAccountIDMetaflowPost($account_id, $metaflow): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Create Account Metaflow

Generate a metaflow for an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID
$metaflow = new \OpenAPI\Client\Model\ServiceVOIPMetaflowAddData(); // \OpenAPI\Client\Model\ServiceVOIPMetaflowAddData | Metaflow fields

try {
    $result = $apiInstance->v1AccountAccountIDMetaflowPost($account_id, $metaflow);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDMetaflowPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID | |
| **metaflow** | [**\OpenAPI\Client\Model\ServiceVOIPMetaflowAddData**](../Model/ServiceVOIPMetaflowAddData.md)| Metaflow fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDUserUserIDMetaflowDelete()`

```php
v1AccountAccountIDUserUserIDMetaflowDelete($account_id, $user_id): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Delete User Metaflow

Delete all metaflows associated with a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$user_id = 'user_id_example'; // string | user ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDUserUserIDMetaflowDelete($account_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDUserUserIDMetaflowDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **user_id** | **string**| user ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDUserUserIDMetaflowGet()`

```php
v1AccountAccountIDUserUserIDMetaflowGet($account_id, $user_id): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Get User Metaflow List

Get the list of metaflows for a user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$user_id = 'user_id_example'; // string | user ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDUserUserIDMetaflowGet($account_id, $user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDUserUserIDMetaflowGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **user_id** | **string**| user ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDUserUserIDMetaflowPost()`

```php
v1AccountAccountIDUserUserIDMetaflowPost($account_id, $user_id, $req_body): \OpenAPI\Client\Model\ServiceDocsMetaflowGet
```

Create User Metaflow

Add a metaflow or multiple metaflows for a user in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MetaflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$user_id = 'user_id_example'; // string | user ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPMetaflowAddData(); // \OpenAPI\Client\Model\ServiceVOIPMetaflowAddData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDUserUserIDMetaflowPost($account_id, $user_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MetaflowApi->v1AccountAccountIDUserUserIDMetaflowPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **user_id** | **string**| user ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPMetaflowAddData**](../Model/ServiceVOIPMetaflowAddData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsMetaflowGet**](../Model/ServiceDocsMetaflowGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
