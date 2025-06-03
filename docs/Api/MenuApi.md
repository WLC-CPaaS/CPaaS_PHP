# OpenAPI\Client\MenuApi

All URIs are relative to http://api.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDMenuGet()**](MenuApi.md#v1AccountAccountIDMenuGet) | **GET** /v1/account/{accountID}/menu | Get Menu List |
| [**v1AccountAccountIDMenuMenuIDDelete()**](MenuApi.md#v1AccountAccountIDMenuMenuIDDelete) | **DELETE** /v1/account/{accountID}/menu/{menuID} | Delete Menu |
| [**v1AccountAccountIDMenuMenuIDGet()**](MenuApi.md#v1AccountAccountIDMenuMenuIDGet) | **GET** /v1/account/{accountID}/menu/{menuID} | Get Menu Details |
| [**v1AccountAccountIDMenuMenuIDPut()**](MenuApi.md#v1AccountAccountIDMenuMenuIDPut) | **PUT** /v1/account/{accountID}/menu/{menuID} | Update Menu |
| [**v1AccountAccountIDMenuPost()**](MenuApi.md#v1AccountAccountIDMenuPost) | **POST** /v1/account/{accountID}/menu | Create Menu |


## `v1AccountAccountIDMenuGet()`

```php
v1AccountAccountIDMenuGet($account_id, $start_key, $page_size): \OpenAPI\Client\Model\MenuOutputList
```

Get Menu List

Users can access data about all menus in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MenuApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountIDMenuGet($account_id, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuApi->v1AccountAccountIDMenuGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\MenuOutputList**](../Model/MenuOutputList.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDMenuMenuIDDelete()`

```php
v1AccountAccountIDMenuMenuIDDelete($account_id, $menu_id): \OpenAPI\Client\Model\MenuOutputDetail
```

Delete Menu

Delete a menu from an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MenuApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$menu_id = 'menu_id_example'; // string | Menu ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDMenuMenuIDDelete($account_id, $menu_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuApi->v1AccountAccountIDMenuMenuIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **menu_id** | **string**| Menu ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\MenuOutputDetail**](../Model/MenuOutputDetail.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDMenuMenuIDGet()`

```php
v1AccountAccountIDMenuMenuIDGet($account_id, $menu_id): \OpenAPI\Client\Model\MenuOutputDetail
```

Get Menu Details

Get details about a menu in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MenuApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$menu_id = 'menu_id_example'; // string | Menu ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDMenuMenuIDGet($account_id, $menu_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuApi->v1AccountAccountIDMenuMenuIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **menu_id** | **string**| Menu ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\MenuOutputDetail**](../Model/MenuOutputDetail.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDMenuMenuIDPut()`

```php
v1AccountAccountIDMenuMenuIDPut($account_id, $menu_id, $req_body): \OpenAPI\Client\Model\MenuOutputDetail
```

Update Menu

Edit an account menu.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MenuApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$menu_id = 'menu_id_example'; // string | Menu ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\MenuInputData(); // \OpenAPI\Client\Model\MenuInputData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDMenuMenuIDPut($account_id, $menu_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuApi->v1AccountAccountIDMenuMenuIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **menu_id** | **string**| Menu ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\MenuInputData**](../Model/MenuInputData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\MenuOutputDetail**](../Model/MenuOutputDetail.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDMenuPost()`

```php
v1AccountAccountIDMenuPost($account_id, $menu): \OpenAPI\Client\Model\MenuOutputDetail
```

Create Menu

Create a new menu for an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MenuApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alphanumeric
$menu = new \OpenAPI\Client\Model\MenuInputData(); // \OpenAPI\Client\Model\MenuInputData | Menu data

try {
    $result = $apiInstance->v1AccountAccountIDMenuPost($account_id, $menu);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MenuApi->v1AccountAccountIDMenuPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alphanumeric | |
| **menu** | [**\OpenAPI\Client\Model\MenuInputData**](../Model/MenuInputData.md)| Menu data | |

### Return type

[**\OpenAPI\Client\Model\MenuOutputDetail**](../Model/MenuOutputDetail.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
