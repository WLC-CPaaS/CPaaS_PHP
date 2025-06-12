# OpenAPI\Client\ProvisionApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDProvisionFilenameGet()**](ProvisionApi.md#v1AccountAccountIDProvisionFilenameGet) | **GET** /v1/account/{accountID}/provision/{filename} |  |


## `v1AccountAccountIDProvisionFilenameGet()`

```php
v1AccountAccountIDProvisionFilenameGet($account_id, $filename): \SplFileObject
```



Retrieve the configuration details (e.g., settings and parameters) for a device.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ProvisionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$filename = 'filename_example'; // string | Name of config file

try {
    $result = $apiInstance->v1AccountAccountIDProvisionFilenameGet($account_id, $filename);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisionApi->v1AccountAccountIDProvisionFilenameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **filename** | **string**| Name of config file | |

### Return type

**\SplFileObject**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
