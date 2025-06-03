# OpenAPI\Client\CallParkApi

All URIs are relative to http://api.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDParkedcallGet()**](CallParkApi.md#v1AccountAccountIDParkedcallGet) | **GET** /v1/account/{accountID}/parkedcall | Get Call Park List |


## `v1AccountAccountIDParkedcallGet()`

```php
v1AccountAccountIDParkedcallGet($account_id): \OpenAPI\Client\Model\ServiceDocsParkedcallGet
```

Get Call Park List

Retrieve a list of calls parked on hold in a numbered slot.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallParkApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDParkedcallGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallParkApi->v1AccountAccountIDParkedcallGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsParkedcallGet**](../Model/ServiceDocsParkedcallGet.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
