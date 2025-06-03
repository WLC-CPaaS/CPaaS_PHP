# OpenAPI\Client\TemporalRuleApi

All URIs are relative to http://api.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDTemporalruleGet()**](TemporalRuleApi.md#v1AccountAccountIDTemporalruleGet) | **GET** /v1/account/{accountID}/temporalrule | Get Temporal Rule List |
| [**v1AccountAccountIDTemporalrulePost()**](TemporalRuleApi.md#v1AccountAccountIDTemporalrulePost) | **POST** /v1/account/{accountID}/temporalrule | Create Temporal Rule |
| [**v1AccountAccountIDTemporalruleTemporalRuleIDDelete()**](TemporalRuleApi.md#v1AccountAccountIDTemporalruleTemporalRuleIDDelete) | **DELETE** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Delete Temporal Rule |
| [**v1AccountAccountIDTemporalruleTemporalRuleIDGet()**](TemporalRuleApi.md#v1AccountAccountIDTemporalruleTemporalRuleIDGet) | **GET** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Get Temporal Rule Details |
| [**v1AccountAccountIDTemporalruleTemporalRuleIDPut()**](TemporalRuleApi.md#v1AccountAccountIDTemporalruleTemporalRuleIDPut) | **PUT** /v1/account/{accountID}/temporalrule/{temporalRuleID} | Update Temporal Rule |


## `v1AccountAccountIDTemporalruleGet()`

```php
v1AccountAccountIDTemporalruleGet($account_id, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsTemporalRuleGetAll
```

Get Temporal Rule List

Access all temporal rules for an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountIDTemporalruleGet($account_id, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleApi->v1AccountAccountIDTemporalruleGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleGetAll**](../Model/ServiceDocsTemporalRuleGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDTemporalrulePost()`

```php
v1AccountAccountIDTemporalrulePost($account_id, $temporalrule): \OpenAPI\Client\Model\ServiceDocsTemporalRuleGetSingle
```

Create Temporal Rule

Create temporal rules for an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alphanumeric
$temporalrule = new \OpenAPI\Client\Model\ServiceVOIPTemporalRuleAddEdit2(); // \OpenAPI\Client\Model\ServiceVOIPTemporalRuleAddEdit2 | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDTemporalrulePost($account_id, $temporalrule);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleApi->v1AccountAccountIDTemporalrulePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alphanumeric | |
| **temporalrule** | [**\OpenAPI\Client\Model\ServiceVOIPTemporalRuleAddEdit2**](../Model/ServiceVOIPTemporalRuleAddEdit2.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleGetSingle**](../Model/ServiceDocsTemporalRuleGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDTemporalruleTemporalRuleIDDelete()`

```php
v1AccountAccountIDTemporalruleTemporalRuleIDDelete($account_id, $temporal_rule_id): \OpenAPI\Client\Model\ServiceDocsTemporalRuleGetSingle
```

Delete Temporal Rule

Remove a temporal rule from an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$temporal_rule_id = 'temporal_rule_id_example'; // string | temporal rule ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDTemporalruleTemporalRuleIDDelete($account_id, $temporal_rule_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleApi->v1AccountAccountIDTemporalruleTemporalRuleIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **temporal_rule_id** | **string**| temporal rule ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleGetSingle**](../Model/ServiceDocsTemporalRuleGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDTemporalruleTemporalRuleIDGet()`

```php
v1AccountAccountIDTemporalruleTemporalRuleIDGet($account_id, $temporal_rule_id): \OpenAPI\Client\Model\ServiceDocsTemporalRuleGetSingle
```

Get Temporal Rule Details

View details about individual time rules.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$temporal_rule_id = 'temporal_rule_id_example'; // string | Temporal Rule ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDTemporalruleTemporalRuleIDGet($account_id, $temporal_rule_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleApi->v1AccountAccountIDTemporalruleTemporalRuleIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **temporal_rule_id** | **string**| Temporal Rule ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleGetSingle**](../Model/ServiceDocsTemporalRuleGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDTemporalruleTemporalRuleIDPut()`

```php
v1AccountAccountIDTemporalruleTemporalRuleIDPut($account_id, $temporal_rule_id, $req_body): \OpenAPI\Client\Model\ServiceDocsTemporalRuleGetSingle
```

Update Temporal Rule

Edit the existing temporal rules in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$temporal_rule_id = 'temporal_rule_id_example'; // string | Temporal Rule ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPTemporalRuleAddEdit2(); // \OpenAPI\Client\Model\ServiceVOIPTemporalRuleAddEdit2 | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDTemporalruleTemporalRuleIDPut($account_id, $temporal_rule_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleApi->v1AccountAccountIDTemporalruleTemporalRuleIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **temporal_rule_id** | **string**| Temporal Rule ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPTemporalRuleAddEdit2**](../Model/ServiceVOIPTemporalRuleAddEdit2.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleGetSingle**](../Model/ServiceDocsTemporalRuleGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
