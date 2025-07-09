# OpenAPI\Client\GroupApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDGroupGet()**](GroupApi.md#v1AccountAccountIDGroupGet) | **GET** /v1/account/{accountID}/group | Get Group List |
| [**v1AccountAccountIDGroupGroupIDDelete()**](GroupApi.md#v1AccountAccountIDGroupGroupIDDelete) | **DELETE** /v1/account/{accountID}/group/{groupID} | Delete Group |
| [**v1AccountAccountIDGroupGroupIDGet()**](GroupApi.md#v1AccountAccountIDGroupGroupIDGet) | **GET** /v1/account/{accountID}/group/{groupID} | Get Group Details |
| [**v1AccountAccountIDGroupGroupIDPut()**](GroupApi.md#v1AccountAccountIDGroupGroupIDPut) | **PUT** /v1/account/{accountID}/group/{groupID} | Update Group |
| [**v1AccountAccountIDGroupPost()**](GroupApi.md#v1AccountAccountIDGroupPost) | **POST** /v1/account/{accountID}/group | Create Group |


## `v1AccountAccountIDGroupGet()`

```php
v1AccountAccountIDGroupGet($account_id, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocGroupGetAll
```

Get Group List

Get a list of groups associated with an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountIDGroupGet($account_id, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->v1AccountAccountIDGroupGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocGroupGetAll**](../Model/ServiceDocGroupGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDGroupGroupIDDelete()`

```php
v1AccountAccountIDGroupGroupIDDelete($account_id, $group_id): \OpenAPI\Client\Model\ServiceDocGroupGetSingle
```

Delete Group

Delete a call group in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$group_id = 'group_id_example'; // string | group ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDGroupGroupIDDelete($account_id, $group_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->v1AccountAccountIDGroupGroupIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **group_id** | **string**| group ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocGroupGetSingle**](../Model/ServiceDocGroupGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDGroupGroupIDGet()`

```php
v1AccountAccountIDGroupGroupIDGet($account_id, $group_id): \OpenAPI\Client\Model\ServiceDocGroupGetSingle
```

Get Group Details

Access details about a single group within an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$group_id = 'group_id_example'; // string | Group ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDGroupGroupIDGet($account_id, $group_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->v1AccountAccountIDGroupGroupIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **group_id** | **string**| Group ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocGroupGetSingle**](../Model/ServiceDocGroupGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDGroupGroupIDPut()`

```php
v1AccountAccountIDGroupGroupIDPut($account_id, $group_id, $req_body): \OpenAPI\Client\Model\ServiceDocGroupGetSingle
```

Update Group

Modify the name, settings and other information for a group within an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$group_id = 'group_id_example'; // string | Group ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPGroupAddEdit2(); // \OpenAPI\Client\Model\ServiceVOIPGroupAddEdit2 | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDGroupGroupIDPut($account_id, $group_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->v1AccountAccountIDGroupGroupIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **group_id** | **string**| Group ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPGroupAddEdit2**](../Model/ServiceVOIPGroupAddEdit2.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocGroupGetSingle**](../Model/ServiceDocGroupGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDGroupPost()`

```php
v1AccountAccountIDGroupPost($account_id, $group): \OpenAPI\Client\Model\ServiceDocGroupGetSingle
```

Create Group

Provide an additional resource by adding a group list to an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID
$group = new \OpenAPI\Client\Model\ServiceVOIPGroupAddEdit2(); // \OpenAPI\Client\Model\ServiceVOIPGroupAddEdit2 | group fields

try {
    $result = $apiInstance->v1AccountAccountIDGroupPost($account_id, $group);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->v1AccountAccountIDGroupPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID | |
| **group** | [**\OpenAPI\Client\Model\ServiceVOIPGroupAddEdit2**](../Model/ServiceVOIPGroupAddEdit2.md)| group fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocGroupGetSingle**](../Model/ServiceDocGroupGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
