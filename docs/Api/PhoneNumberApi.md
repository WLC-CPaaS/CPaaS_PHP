# OpenAPI\Client\PhoneNumberApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountidPhonenumberGet()**](PhoneNumberApi.md#v1AccountAccountidPhonenumberGet) | **GET** /v1/account/{accountid}/phonenumber | Get Assigned Numbers List |
| [**v1AccountPhonenumberAssignPost()**](PhoneNumberApi.md#v1AccountPhonenumberAssignPost) | **POST** /v1/account/phonenumber/assign | Assign Number |
| [**v1AccountPhonenumberDisconnectPost()**](PhoneNumberApi.md#v1AccountPhonenumberDisconnectPost) | **POST** /v1/account/phonenumber/disconnect | Disconnect Number |
| [**v1AccountPhonenumberGet()**](PhoneNumberApi.md#v1AccountPhonenumberGet) | **GET** /v1/account/phonenumber | Get Unassigned Numbers List |
| [**v1AccountPhonenumberPost()**](PhoneNumberApi.md#v1AccountPhonenumberPost) | **POST** /v1/account/phonenumber | Purchase Number |
| [**v1AccountPhonenumberUnassignPost()**](PhoneNumberApi.md#v1AccountPhonenumberUnassignPost) | **POST** /v1/account/phonenumber/unassign | Unassign Number |
| [**v1PhonenumberSearchGet()**](PhoneNumberApi.md#v1PhonenumberSearchGet) | **GET** /v1/phonenumber/search | Search New Numbers |


## `v1AccountAccountidPhonenumberGet()`

```php
v1AccountAccountidPhonenumberGet($accountid, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsAccountPhonenumberGetAll
```

Get Assigned Numbers List

Access all phone numbers assigned to a CPaaS account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PhoneNumberApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | Start key for pagination, obtained from previous responses
$page_size = 56; // int | Number of records to return per page (range: 1 to 50)

try {
    $result = $apiInstance->v1AccountAccountidPhonenumberGet($accountid, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PhoneNumberApi->v1AccountAccountidPhonenumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| Start key for pagination, obtained from previous responses | [optional] |
| **page_size** | **int**| Number of records to return per page (range: 1 to 50) | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountPhonenumberGetAll**](../Model/ServiceDocsAccountPhonenumberGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountPhonenumberAssignPost()`

```php
v1AccountPhonenumberAssignPost($payload): \OpenAPI\Client\Model\ServiceAPIResponseStatusCodeOnly
```

Assign Number

Assign a purchased phone number to an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PhoneNumberApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payload = new \OpenAPI\Client\Model\ServiceDocsPhonenumberAssignPayload(); // \OpenAPI\Client\Model\ServiceDocsPhonenumberAssignPayload | assignment payload

try {
    $result = $apiInstance->v1AccountPhonenumberAssignPost($payload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PhoneNumberApi->v1AccountPhonenumberAssignPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payload** | [**\OpenAPI\Client\Model\ServiceDocsPhonenumberAssignPayload**](../Model/ServiceDocsPhonenumberAssignPayload.md)| assignment payload | |

### Return type

[**\OpenAPI\Client\Model\ServiceAPIResponseStatusCodeOnly**](../Model/ServiceAPIResponseStatusCodeOnly.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountPhonenumberDisconnectPost()`

```php
v1AccountPhonenumberDisconnectPost($payload): \OpenAPI\Client\Model\ServiceAPIResponseStatusCodeOnly
```

Disconnect Number

Disconnecting a phone number from a CPaaS account relinquishes ownership of the number back to the carrier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PhoneNumberApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payload = new \OpenAPI\Client\Model\ServiceDocsPhonenumberUnassignPayload(); // \OpenAPI\Client\Model\ServiceDocsPhonenumberUnassignPayload | disconnect payload

try {
    $result = $apiInstance->v1AccountPhonenumberDisconnectPost($payload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PhoneNumberApi->v1AccountPhonenumberDisconnectPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payload** | [**\OpenAPI\Client\Model\ServiceDocsPhonenumberUnassignPayload**](../Model/ServiceDocsPhonenumberUnassignPayload.md)| disconnect payload | |

### Return type

[**\OpenAPI\Client\Model\ServiceAPIResponseStatusCodeOnly**](../Model/ServiceAPIResponseStatusCodeOnly.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountPhonenumberGet()`

```php
v1AccountPhonenumberGet($start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsAccountPhonenumberGetAll
```

Get Unassigned Numbers List

Obtain all phone numbers that have not been assigned to a CPaaS account within your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PhoneNumberApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_key = 'start_key_example'; // string | Start key for pagination, obtained from previous responses
$page_size = 56; // int | Number of records to return per page (range: 1 to 50)

try {
    $result = $apiInstance->v1AccountPhonenumberGet($start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PhoneNumberApi->v1AccountPhonenumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **start_key** | **string**| Start key for pagination, obtained from previous responses | [optional] |
| **page_size** | **int**| Number of records to return per page (range: 1 to 50) | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountPhonenumberGetAll**](../Model/ServiceDocsAccountPhonenumberGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountPhonenumberPost()`

```php
v1AccountPhonenumberPost($phonenumber): \OpenAPI\Client\Model\ServiceDocsOrderPhonenumber
```

Purchase Number

Purchase or activate a phone number for CPaaS accounts within your business.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PhoneNumberApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$phonenumber = array('phonenumber_example'); // string[] | phonenumber fields

try {
    $result = $apiInstance->v1AccountPhonenumberPost($phonenumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PhoneNumberApi->v1AccountPhonenumberPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phonenumber** | [**string[]**](../Model/string.md)| phonenumber fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsOrderPhonenumber**](../Model/ServiceDocsOrderPhonenumber.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountPhonenumberUnassignPost()`

```php
v1AccountPhonenumberUnassignPost($payload): \OpenAPI\Client\Model\ServiceAPIResponseStatusCodeOnly
```

Unassign Number

Remove a phone number from an account and place it back on the list of unassigned phone numbers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PhoneNumberApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$payload = new \OpenAPI\Client\Model\ServiceDocsPhonenumberUnassignPayload(); // \OpenAPI\Client\Model\ServiceDocsPhonenumberUnassignPayload | unassign payload

try {
    $result = $apiInstance->v1AccountPhonenumberUnassignPost($payload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PhoneNumberApi->v1AccountPhonenumberUnassignPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payload** | [**\OpenAPI\Client\Model\ServiceDocsPhonenumberUnassignPayload**](../Model/ServiceDocsPhonenumberUnassignPayload.md)| unassign payload | |

### Return type

[**\OpenAPI\Client\Model\ServiceAPIResponseStatusCodeOnly**](../Model/ServiceAPIResponseStatusCodeOnly.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1PhonenumberSearchGet()`

```php
v1PhonenumberSearchGet($area_code, $quantity): \OpenAPI\Client\Model\ServiceDocsPhonenumberSearchGetAll
```

Search New Numbers

Conduct a search for available phone numbers for purchase within an area code.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\PhoneNumberApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$area_code = 'area_code_example'; // string | Area code (exactly 3 numeric characters) example: 610 or 484
$quantity = 100; // int | Number of records to return (range: 1 to 100, defaults to 100 if not provided)

try {
    $result = $apiInstance->v1PhonenumberSearchGet($area_code, $quantity);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PhoneNumberApi->v1PhonenumberSearchGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **area_code** | **string**| Area code (exactly 3 numeric characters) example: 610 or 484 | |
| **quantity** | **int**| Number of records to return (range: 1 to 100, defaults to 100 if not provided) | [optional] [default to 100] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsPhonenumberSearchGetAll**](../Model/ServiceDocsPhonenumberSearchGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
