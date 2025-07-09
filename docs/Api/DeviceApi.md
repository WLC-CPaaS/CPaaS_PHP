# OpenAPI\Client\DeviceApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountidDeviceDeviceidDelete()**](DeviceApi.md#v1AccountAccountidDeviceDeviceidDelete) | **DELETE** /v1/account/{accountid}/device/{deviceid} | Delete Device |
| [**v1AccountAccountidDeviceDeviceidGet()**](DeviceApi.md#v1AccountAccountidDeviceDeviceidGet) | **GET** /v1/account/{accountid}/device/{deviceid} | Get Device Details |
| [**v1AccountAccountidDeviceDeviceidPut()**](DeviceApi.md#v1AccountAccountidDeviceDeviceidPut) | **PUT** /v1/account/{accountid}/device/{deviceid} | Update Device |
| [**v1AccountAccountidDeviceDeviceidRebootPost()**](DeviceApi.md#v1AccountAccountidDeviceDeviceidRebootPost) | **POST** /v1/account/{accountid}/device/{deviceid}/reboot | Reboot Device |
| [**v1AccountAccountidDeviceGet()**](DeviceApi.md#v1AccountAccountidDeviceGet) | **GET** /v1/account/{accountid}/device | Get Device List |
| [**v1AccountAccountidDevicePost()**](DeviceApi.md#v1AccountAccountidDevicePost) | **POST** /v1/account/{accountid}/device | Create Device |
| [**v1AccountAccountidDeviceStatusGet()**](DeviceApi.md#v1AccountAccountidDeviceStatusGet) | **GET** /v1/account/{accountid}/device/status | Get Device Status |


## `v1AccountAccountidDeviceDeviceidDelete()`

```php
v1AccountAccountidDeviceDeviceidDelete($accountid, $deviceid): \OpenAPI\Client\Model\ServiceDocsDeviceGetSingle
```

Delete Device

Remove one device from a CPaaS account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$deviceid = 'deviceid_example'; // string | Device ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidDeviceDeviceidDelete($accountid, $deviceid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->v1AccountAccountidDeviceDeviceidDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **deviceid** | **string**| Device ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsDeviceGetSingle**](../Model/ServiceDocsDeviceGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDeviceDeviceidGet()`

```php
v1AccountAccountidDeviceDeviceidGet($accountid, $deviceid): \OpenAPI\Client\Model\ServiceDocsDeviceGetSingle
```

Get Device Details

Permit a user to view specific device details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$deviceid = 'deviceid_example'; // string | Device ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidDeviceDeviceidGet($accountid, $deviceid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->v1AccountAccountidDeviceDeviceidGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **deviceid** | **string**| Device ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsDeviceGetSingle**](../Model/ServiceDocsDeviceGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDeviceDeviceidPut()`

```php
v1AccountAccountidDeviceDeviceidPut($accountid, $deviceid, $device): \OpenAPI\Client\Model\ServiceDocsDeviceGetSingle
```

Update Device

Edit specifics about the device, such as the device type, name, and owner.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$deviceid = 'deviceid_example'; // string | Device ID, 32 alpha numeric
$device = new \OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit2(); // \OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit2 | device fields

try {
    $result = $apiInstance->v1AccountAccountidDeviceDeviceidPut($accountid, $deviceid, $device);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->v1AccountAccountidDeviceDeviceidPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **deviceid** | **string**| Device ID, 32 alpha numeric | |
| **device** | [**\OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit2**](../Model/ServiceVOIPDeviceAddEdit2.md)| device fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsDeviceGetSingle**](../Model/ServiceDocsDeviceGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDeviceDeviceidRebootPost()`

```php
v1AccountAccountidDeviceDeviceidRebootPost($accountid, $deviceid): \OpenAPI\Client\Model\ServiceDocsDeviceReboot
```

Reboot Device

Reboot a device in an account to mitigate malware and improve device performance.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$deviceid = 'deviceid_example'; // string | Device ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidDeviceDeviceidRebootPost($accountid, $deviceid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->v1AccountAccountidDeviceDeviceidRebootPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **deviceid** | **string**| Device ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsDeviceReboot**](../Model/ServiceDocsDeviceReboot.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDeviceGet()`

```php
v1AccountAccountidDeviceGet($accountid, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsDeviceGetAll
```

Get Device List

Obtain a list of all devices associated with an account such as fax machines, cell phones, and soft phones.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountidDeviceGet($accountid, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->v1AccountAccountidDeviceGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsDeviceGetAll**](../Model/ServiceDocsDeviceGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDevicePost()`

```php
v1AccountAccountidDevicePost($accountid, $device): \OpenAPI\Client\Model\ServiceDocsDeviceGetSingle
```

Create Device

Connect a new device to an account to enhance communication methods.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$device = new \OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit2(); // \OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit2 | device fields

try {
    $result = $apiInstance->v1AccountAccountidDevicePost($accountid, $device);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->v1AccountAccountidDevicePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **device** | [**\OpenAPI\Client\Model\ServiceVOIPDeviceAddEdit2**](../Model/ServiceVOIPDeviceAddEdit2.md)| device fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsDeviceGetSingle**](../Model/ServiceDocsDeviceGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDeviceStatusGet()`

```php
v1AccountAccountidDeviceStatusGet($accountid): \OpenAPI\Client\Model\ServiceDocsDeviceStatus
```

Get Device Status

Retrieve a device’s status (e.g., registered or not registered) in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidDeviceStatusGet($accountid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->v1AccountAccountidDeviceStatusGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsDeviceStatus**](../Model/ServiceDocsDeviceStatus.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
