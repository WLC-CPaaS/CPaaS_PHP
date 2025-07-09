# OpenAPI\Client\TemporalRuleSetApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDTemporalrulesetGet()**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetGet) | **GET** /v1/account/{accountID}/temporalruleset | Get Temporal Rule Set List |
| [**v1AccountAccountIDTemporalrulesetPost()**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetPost) | **POST** /v1/account/{accountID}/temporalruleset | Create Temporal Rule Set |
| [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete()**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete) | **DELETE** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Delete Temporal Rule Set |
| [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet()**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet) | **GET** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Get Temporal Rule Set Details |
| [**v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut()**](TemporalRuleSetApi.md#v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut) | **PUT** /v1/account/{accountID}/temporalruleset/{temporalRuleSetID} | Update Temporal Rule Set |


## `v1AccountAccountIDTemporalrulesetGet()`

```php
v1AccountAccountIDTemporalrulesetGet($account_id, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetAll
```

Get Temporal Rule Set List

Access the temporal rule set list in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleSetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountIDTemporalrulesetGet($account_id, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleSetApi->v1AccountAccountIDTemporalrulesetGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetAll**](../Model/ServiceDocsTemporalRuleSetGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDTemporalrulesetPost()`

```php
v1AccountAccountIDTemporalrulesetPost($account_id, $temporalruleset): \OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetSingle
```

Create Temporal Rule Set

Develop a new temporal rule set for an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleSetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alphanumeric
$temporalruleset = new \OpenAPI\Client\Model\ServiceVOIPTemporalRuleSetAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPTemporalRuleSetAddEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDTemporalrulesetPost($account_id, $temporalruleset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleSetApi->v1AccountAccountIDTemporalrulesetPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alphanumeric | |
| **temporalruleset** | [**\OpenAPI\Client\Model\ServiceVOIPTemporalRuleSetAddEditData**](../Model/ServiceVOIPTemporalRuleSetAddEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetSingle**](../Model/ServiceDocsTemporalRuleSetGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete()`

```php
v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete($account_id, $temporal_rule_set_id): \OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetSingle
```

Delete Temporal Rule Set

Delete the temporal rule set from an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleSetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$temporal_rule_set_id = 'temporal_rule_set_id_example'; // string | temporal rule set ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete($account_id, $temporal_rule_set_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleSetApi->v1AccountAccountIDTemporalrulesetTemporalRuleSetIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **temporal_rule_set_id** | **string**| temporal rule set ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetSingle**](../Model/ServiceDocsTemporalRuleSetGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet()`

```php
v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet($account_id, $temporal_rule_set_id): \OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetSingle
```

Get Temporal Rule Set Details

Acquire details about a temporal rule set in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleSetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$temporal_rule_set_id = 'temporal_rule_set_id_example'; // string | Temporal Ruleset ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet($account_id, $temporal_rule_set_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleSetApi->v1AccountAccountIDTemporalrulesetTemporalRuleSetIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **temporal_rule_set_id** | **string**| Temporal Ruleset ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetSingle**](../Model/ServiceDocsTemporalRuleSetGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut()`

```php
v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut($account_id, $temporal_rule_set_id, $req_body): \OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetSingle
```

Update Temporal Rule Set

Efficiently adjust the temporal rule set in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\TemporalRuleSetApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$temporal_rule_set_id = 'temporal_rule_set_id_example'; // string | Temporal Ruleset ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPTemporalRuleSetAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPTemporalRuleSetAddEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut($account_id, $temporal_rule_set_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemporalRuleSetApi->v1AccountAccountIDTemporalrulesetTemporalRuleSetIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **temporal_rule_set_id** | **string**| Temporal Ruleset ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPTemporalRuleSetAddEditData**](../Model/ServiceVOIPTemporalRuleSetAddEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsTemporalRuleSetGetSingle**](../Model/ServiceDocsTemporalRuleSetGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
