# OpenAPI\Client\AccountApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountidChildrenGet()**](AccountApi.md#v1AccountAccountidChildrenGet) | **GET** /v1/account/{accountid}/children | Get Sub Account List |
| [**v1AccountAccountidDelete()**](AccountApi.md#v1AccountAccountidDelete) | **DELETE** /v1/account/{accountid} | Delete Account |
| [**v1AccountAccountidDnsrecordGet()**](AccountApi.md#v1AccountAccountidDnsrecordGet) | **GET** /v1/account/{accountid}/dnsrecord | Get Account DNS Record |
| [**v1AccountAccountidDnsrecordPost()**](AccountApi.md#v1AccountAccountidDnsrecordPost) | **POST** /v1/account/{accountid}/dnsrecord | Create Account DNS Record |
| [**v1AccountAccountidDnsrecordPut()**](AccountApi.md#v1AccountAccountidDnsrecordPut) | **PUT** /v1/account/{accountid}/dnsrecord | Convert Account DNS Record |
| [**v1AccountAccountidGet()**](AccountApi.md#v1AccountAccountidGet) | **GET** /v1/account/{accountid} | Get Account Details |
| [**v1AccountAccountidLimitGet()**](AccountApi.md#v1AccountAccountidLimitGet) | **GET** /v1/account/{accountid}/limit | Get Account Limits |
| [**v1AccountAccountidLimitPut()**](AccountApi.md#v1AccountAccountidLimitPut) | **PUT** /v1/account/{accountid}/limit | Set Account Limits |
| [**v1AccountAccountidPost()**](AccountApi.md#v1AccountAccountidPost) | **POST** /v1/account/{accountid} | Create Sub Account |
| [**v1AccountAccountidProvisioningdetailsGet()**](AccountApi.md#v1AccountAccountidProvisioningdetailsGet) | **GET** /v1/account/{accountid}/provisioningdetails | Get Account Provisioning Details |
| [**v1AccountAccountidProvisioningdetailsResetpwPut()**](AccountApi.md#v1AccountAccountidProvisioningdetailsResetpwPut) | **PUT** /v1/account/{accountid}/provisioningdetails/resetpw | Reset the provisioning details password. |
| [**v1AccountAccountidPut()**](AccountApi.md#v1AccountAccountidPut) | **PUT** /v1/account/{accountid} | Update Account |
| [**v1AccountApikeyGet()**](AccountApi.md#v1AccountApikeyGet) | **GET** /v1/account/apikey |  |
| [**v1AccountGet()**](AccountApi.md#v1AccountGet) | **GET** /v1/account | Get Account List |
| [**v1AccountPost()**](AccountApi.md#v1AccountPost) | **POST** /v1/account | Create Account |


## `v1AccountAccountidChildrenGet()`

```php
v1AccountAccountidChildrenGet($accountid, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsAccountGetAll
```

Get Sub Account List

Conveniently access the list of children accounts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountidChildrenGet($accountid, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidChildrenGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetAll**](../Model/ServiceDocsAccountGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDelete()`

```php
v1AccountAccountidDelete($accountid): \OpenAPI\Client\Model\ServiceDocsAccountGetSingle
```

Delete Account

Delete an account within your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidDelete($accountid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetSingle**](../Model/ServiceDocsAccountGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDnsrecordGet()`

```php
v1AccountAccountidDnsrecordGet($accountid): \OpenAPI\Client\Model\ServiceDocsAccountGetSingle
```

Get Account DNS Record

Get the DNS record of an account from the Route 53 entry.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidDnsrecordGet($accountid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidDnsrecordGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetSingle**](../Model/ServiceDocsAccountGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDnsrecordPost()`

```php
v1AccountAccountidDnsrecordPost($accountid): \OpenAPI\Client\Model\ServiceDocsAccountGetSingle
```

Create Account DNS Record

Create the DNS record of an account with the help realm in the Route 53 entry.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidDnsrecordPost($accountid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidDnsrecordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetSingle**](../Model/ServiceDocsAccountGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidDnsrecordPut()`

```php
v1AccountAccountidDnsrecordPut($accountid, $dnsrecord): \OpenAPI\Client\Model\ServiceDocsAccountGetSingle
```

Convert Account DNS Record

Toggle the realm DNS record between srv and cname.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$dnsrecord = new \OpenAPI\Client\Model\ServiceUpdateRecordTypeForAccount(); // \OpenAPI\Client\Model\ServiceUpdateRecordTypeForAccount | record type fields with value SRV, CNAME

try {
    $result = $apiInstance->v1AccountAccountidDnsrecordPut($accountid, $dnsrecord);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidDnsrecordPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **dnsrecord** | [**\OpenAPI\Client\Model\ServiceUpdateRecordTypeForAccount**](../Model/ServiceUpdateRecordTypeForAccount.md)| record type fields with value SRV, CNAME | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetSingle**](../Model/ServiceDocsAccountGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidGet()`

```php
v1AccountAccountidGet($accountid): \OpenAPI\Client\Model\ServiceDocsAccountGetSingle
```

Get Account Details

This endpoint will not allow for modifying or making updates, it will only allow users to view/retrieve details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidGet($accountid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetSingle**](../Model/ServiceDocsAccountGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidLimitGet()`

```php
v1AccountAccountidLimitGet($accountid): \OpenAPI\Client\Model\ServiceDocsAccountLimit
```

Get Account Limits

Check the maximum number of inbound, outbound, and two-way trunks.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidLimitGet($accountid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidLimitGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountLimit**](../Model/ServiceDocsAccountLimit.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidLimitPut()`

```php
v1AccountAccountidLimitPut($accountid, $limit): \OpenAPI\Client\Model\ServiceDocsAccountLimit
```

Set Account Limits

Apply parameters to restrict access to inbound, outbound, and two-way trunks.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$limit = new \OpenAPI\Client\Model\ServiceVOIPAccountLimit2(); // \OpenAPI\Client\Model\ServiceVOIPAccountLimit2 | account fields

try {
    $result = $apiInstance->v1AccountAccountidLimitPut($accountid, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidLimitPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **limit** | [**\OpenAPI\Client\Model\ServiceVOIPAccountLimit2**](../Model/ServiceVOIPAccountLimit2.md)| account fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountLimit**](../Model/ServiceDocsAccountLimit.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidPost()`

```php
v1AccountAccountidPost($accountid, $account): \OpenAPI\Client\Model\ServiceDocsAccountGetSingle
```

Create Sub Account

Establish a sub account to enable an administrator within your organization to create accounts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$account = new \OpenAPI\Client\Model\ServiceVOIPAccountAddData(); // \OpenAPI\Client\Model\ServiceVOIPAccountAddData | account fields

try {
    $result = $apiInstance->v1AccountAccountidPost($accountid, $account);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **account** | [**\OpenAPI\Client\Model\ServiceVOIPAccountAddData**](../Model/ServiceVOIPAccountAddData.md)| account fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetSingle**](../Model/ServiceDocsAccountGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidProvisioningdetailsGet()`

```php
v1AccountAccountidProvisioningdetailsGet($accountid): \OpenAPI\Client\Model\ServiceDocsAccountProvisioning
```

Get Account Provisioning Details

Get the provisioning details of an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidProvisioningdetailsGet($accountid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidProvisioningdetailsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountProvisioning**](../Model/ServiceDocsAccountProvisioning.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidProvisioningdetailsResetpwPut()`

```php
v1AccountAccountidProvisioningdetailsResetpwPut($accountid): \OpenAPI\Client\Model\ServiceDocsAccountProvisioning
```

Reset the provisioning details password.

Reset the existing provisioning details password and set it to a new one.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidProvisioningdetailsResetpwPut($accountid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidProvisioningdetailsResetpwPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountProvisioning**](../Model/ServiceDocsAccountProvisioning.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidPut()`

```php
v1AccountAccountidPut($accountid, $account): \OpenAPI\Client\Model\ServiceDocsAccountGetSingle
```

Update Account

Modify pertinent account data.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$account = new \OpenAPI\Client\Model\ServiceVOIPAccountEditData(); // \OpenAPI\Client\Model\ServiceVOIPAccountEditData | account fields

try {
    $result = $apiInstance->v1AccountAccountidPut($accountid, $account);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountAccountidPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **account** | [**\OpenAPI\Client\Model\ServiceVOIPAccountEditData**](../Model/ServiceVOIPAccountEditData.md)| account fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetSingle**](../Model/ServiceDocsAccountGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountApikeyGet()`

```php
v1AccountApikeyGet(): \OpenAPI\Client\Model\ServiceDocsAccountAPIKey
```



Authenticate an application or user request to get the client ID and client secret for a CPaaS account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->v1AccountApikeyGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountApikeyGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountAPIKey**](../Model/ServiceDocsAccountAPIKey.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountGet()`

```php
v1AccountGet($start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsAccountGetAll
```

Get Account List

Retrieve a list of all CPaaS accounts that exist within your organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountGet($start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetAll**](../Model/ServiceDocsAccountGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountPost()`

```php
v1AccountPost($account): \OpenAPI\Client\Model\ServiceDocsAccountGetSingle
```

Create Account

Create an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account = new \OpenAPI\Client\Model\ServiceVOIPAccountAddData(); // \OpenAPI\Client\Model\ServiceVOIPAccountAddData | account fields

try {
    $result = $apiInstance->v1AccountPost($account);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->v1AccountPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account** | [**\OpenAPI\Client\Model\ServiceVOIPAccountAddData**](../Model/ServiceVOIPAccountAddData.md)| account fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAccountGetSingle**](../Model/ServiceDocsAccountGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
