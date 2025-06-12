# OpenAPI\Client\CallflowApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDCallflowCallflowIDDelete()**](CallflowApi.md#v1AccountAccountIDCallflowCallflowIDDelete) | **DELETE** /v1/account/{accountID}/callflow/{callflowID} | Delete Call Group |
| [**v1AccountAccountIDCallflowCallflowIDGet()**](CallflowApi.md#v1AccountAccountIDCallflowCallflowIDGet) | **GET** /v1/account/{accountID}/callflow/{callflowID} | Get Call Group Details |
| [**v1AccountAccountIDCallflowCallflowIDPut()**](CallflowApi.md#v1AccountAccountIDCallflowCallflowIDPut) | **PUT** /v1/account/{accountID}/callflow/{callflowID} | Update Call Group |
| [**v1AccountAccountIDCallflowGet()**](CallflowApi.md#v1AccountAccountIDCallflowGet) | **GET** /v1/account/{accountID}/callflow | Get Callflow List |
| [**v1AccountAccountIDCallflowPost()**](CallflowApi.md#v1AccountAccountIDCallflowPost) | **POST** /v1/account/{accountID}/callflow | Create Call Group |


## `v1AccountAccountIDCallflowCallflowIDDelete()`

```php
v1AccountAccountIDCallflowCallflowIDDelete($account_id, $callflow_id): \OpenAPI\Client\Model\ServiceDocsCallflowGetSingle
```

Delete Call Group

Delete a callflow in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$callflow_id = 'callflow_id_example'; // string | callflow ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDCallflowCallflowIDDelete($account_id, $callflow_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallflowApi->v1AccountAccountIDCallflowCallflowIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **callflow_id** | **string**| callflow ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallflowGetSingle**](../Model/ServiceDocsCallflowGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallflowCallflowIDGet()`

```php
v1AccountAccountIDCallflowCallflowIDGet($account_id, $callflow_id): \OpenAPI\Client\Model\ServiceDocsCallflowGetSingle
```

Get Call Group Details

Get the details for a single callflow in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$callflow_id = 'callflow_id_example'; // string | Callflow ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDCallflowCallflowIDGet($account_id, $callflow_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallflowApi->v1AccountAccountIDCallflowCallflowIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **callflow_id** | **string**| Callflow ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallflowGetSingle**](../Model/ServiceDocsCallflowGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallflowCallflowIDPut()`

```php
v1AccountAccountIDCallflowCallflowIDPut($account_id, $callflow_id, $req_body): \OpenAPI\Client\Model\ServiceDocsCallflowGetSingle
```

Update Call Group

Update the details for a single callflow in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$callflow_id = 'callflow_id_example'; // string | Callflow ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceCallflowAddEditData(); // \OpenAPI\Client\Model\ServiceCallflowAddEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDCallflowCallflowIDPut($account_id, $callflow_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallflowApi->v1AccountAccountIDCallflowCallflowIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **callflow_id** | **string**| Callflow ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceCallflowAddEditData**](../Model/ServiceCallflowAddEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallflowGetSingle**](../Model/ServiceDocsCallflowGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallflowGet()`

```php
v1AccountAccountIDCallflowGet($account_id, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsCallflowGetAll
```

Get Callflow List

Permit a user to view the callflow details in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountIDCallflowGet($account_id, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallflowApi->v1AccountAccountIDCallflowGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallflowGetAll**](../Model/ServiceDocsCallflowGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallflowPost()`

```php
v1AccountAccountIDCallflowPost($account_id, $request): \OpenAPI\Client\Model\ServiceDocsCallflowGetSingle
```

Create Call Group

Create instructions for routing a call to a user or system.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallflowApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha-numeric
$request = new \OpenAPI\Client\Model\ServiceCallflowAddEditData(); // \OpenAPI\Client\Model\ServiceCallflowAddEditData | Call flow configuration

try {
    $result = $apiInstance->v1AccountAccountIDCallflowPost($account_id, $request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallflowApi->v1AccountAccountIDCallflowPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha-numeric | |
| **request** | [**\OpenAPI\Client\Model\ServiceCallflowAddEditData**](../Model/ServiceCallflowAddEditData.md)| Call flow configuration | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallflowGetSingle**](../Model/ServiceDocsCallflowGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
