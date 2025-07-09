# OpenAPI\Client\DataApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDCdrCdrIDGet()**](DataApi.md#v1AccountAccountIDCdrCdrIDGet) | **GET** /v1/account/{accountID}/cdr/{cdrID} | Get CDR Details |
| [**v1AccountAccountIDCdrGet()**](DataApi.md#v1AccountAccountIDCdrGet) | **GET** /v1/account/{accountID}/cdr | Get CDR List |
| [**v1DataCallDailySummaryGet()**](DataApi.md#v1DataCallDailySummaryGet) | **GET** /v1/data/call_daily_summary | Get Call Daily Summary List |
| [**v1DataCallDetailGet()**](DataApi.md#v1DataCallDetailGet) | **GET** /v1/data/call_detail | Get Call Detail List |
| [**v1DataCallMonthlySummaryGet()**](DataApi.md#v1DataCallMonthlySummaryGet) | **GET** /v1/data/call_monthly_summary | Get Call Detail List |
| [**v1DataEndpointListGet()**](DataApi.md#v1DataEndpointListGet) | **GET** /v1/data/endpoint_list | Get Endpoint List |
| [**v1DataEventDailySummaryGet()**](DataApi.md#v1DataEventDailySummaryGet) | **GET** /v1/data/event_daily_summary | Get Event Daily Summary List |
| [**v1DataEventDetailGet()**](DataApi.md#v1DataEventDetailGet) | **GET** /v1/data/event_detail | Get Event Details |
| [**v1DataEventMonthlySummaryGet()**](DataApi.md#v1DataEventMonthlySummaryGet) | **GET** /v1/data/event_monthly_summary | Get Event Monthly Summary List |
| [**v1DataFeatureDailySummaryGet()**](DataApi.md#v1DataFeatureDailySummaryGet) | **GET** /v1/data/feature_daily_summary | Get Feature Daily Summary List |
| [**v1DataFeatureMonthlySummaryGet()**](DataApi.md#v1DataFeatureMonthlySummaryGet) | **GET** /v1/data/feature_monthly_summary | Get Feature Monthly Summary List |


## `v1AccountAccountIDCdrCdrIDGet()`

```php
v1AccountAccountIDCdrCdrIDGet($account_id, $cdr_id): \OpenAPI\Client\Model\ServiceDocsCdrGetSingle
```

Get CDR Details

Retrieve the details of a single CDR record from an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$cdr_id = 'cdr_id_example'; // string | CDR ID, string

try {
    $result = $apiInstance->v1AccountAccountIDCdrCdrIDGet($account_id, $cdr_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1AccountAccountIDCdrCdrIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **cdr_id** | **string**| CDR ID, string | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCdrGetSingle**](../Model/ServiceDocsCdrGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCdrGet()`

```php
v1AccountAccountIDCdrGet($account_id, $page_size, $start_key, $created_from, $created_to): \OpenAPI\Client\Model\ServiceDocsCdrGetAll
```

Get CDR List

Retrieve a list of CDRs in a specific account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$page_size = 'page_size_example'; // string | Page size (Maximum number of results to display per page)
$start_key = 'start_key_example'; // string | Start key (Starting offset for displaying results)
$created_from = 'created_from_example'; // string | For displaying records which are created on or after this timestamp (Supported timestamp formats: iso 8601, unix time in seconds or milliseconds or microseconds or nanoseconds)
$created_to = 'created_to_example'; // string | For displaying records which are created on or before this timestamp (Supported timestamp formats: iso 8601, unix time in seconds or milliseconds or microseconds or nanoseconds)

try {
    $result = $apiInstance->v1AccountAccountIDCdrGet($account_id, $page_size, $start_key, $created_from, $created_to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1AccountAccountIDCdrGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **page_size** | **string**| Page size (Maximum number of results to display per page) | [optional] |
| **start_key** | **string**| Start key (Starting offset for displaying results) | [optional] |
| **created_from** | **string**| For displaying records which are created on or after this timestamp (Supported timestamp formats: iso 8601, unix time in seconds or milliseconds or microseconds or nanoseconds) | [optional] |
| **created_to** | **string**| For displaying records which are created on or before this timestamp (Supported timestamp formats: iso 8601, unix time in seconds or milliseconds or microseconds or nanoseconds) | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCdrGetAll**](../Model/ServiceDocsCdrGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataCallDailySummaryGet()`

```php
v1DataCallDailySummaryGet($account_id, $call_type, $end_date, $page_size, $start_date, $start_key): \OpenAPI\Client\Model\ServiceDocsCallDailySummary
```

Get Call Daily Summary List

Retrieve a daily summary of calls, including the account ID that made or received a call, the call type, the month and year, the duration, and other relevant information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$call_type = 'call_type_example'; // string
$end_date = 'end_date_example'; // string
$page_size = 56; // int
$start_date = 'start_date_example'; // string
$start_key = 'start_key_example'; // string

try {
    $result = $apiInstance->v1DataCallDailySummaryGet($account_id, $call_type, $end_date, $page_size, $start_date, $start_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataCallDailySummaryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | [optional] |
| **call_type** | **string**|  | [optional] |
| **end_date** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_date** | **string**|  | [optional] |
| **start_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallDailySummary**](../Model/ServiceDocsCallDailySummary.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataCallDetailGet()`

```php
v1DataCallDetailGet($account, $call_type, $callee_name, $callee_number, $caller_name, $caller_number, $end_date, $page_size, $start_date, $start_key): \OpenAPI\Client\Model\ServiceDocsCallDetail
```

Get Call Detail List

Retrieve specific details about a call (e.g., caller, recipient, date, time, duration, etc.).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account = 'account_example'; // string
$call_type = 'call_type_example'; // string
$callee_name = 'callee_name_example'; // string
$callee_number = 'callee_number_example'; // string
$caller_name = 'caller_name_example'; // string
$caller_number = 'caller_number_example'; // string
$end_date = 'end_date_example'; // string
$page_size = 56; // int
$start_date = 'start_date_example'; // string
$start_key = 'start_key_example'; // string

try {
    $result = $apiInstance->v1DataCallDetailGet($account, $call_type, $callee_name, $callee_number, $caller_name, $caller_number, $end_date, $page_size, $start_date, $start_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataCallDetailGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account** | **string**|  | [optional] |
| **call_type** | **string**|  | [optional] |
| **callee_name** | **string**|  | [optional] |
| **callee_number** | **string**|  | [optional] |
| **caller_name** | **string**|  | [optional] |
| **caller_number** | **string**|  | [optional] |
| **end_date** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_date** | **string**|  | [optional] |
| **start_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallDetail**](../Model/ServiceDocsCallDetail.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataCallMonthlySummaryGet()`

```php
v1DataCallMonthlySummaryGet($account, $call_type, $end_month, $end_year, $page_size, $start_key, $start_month, $start_year): \OpenAPI\Client\Model\ServiceDocsCallMonthlySummary
```

Get Call Detail List

Retrieve a monthly summary of calls, including which accounts made or received calls, the call type, and other relevant information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account = 'account_example'; // string
$call_type = 'call_type_example'; // string
$end_month = 56; // int
$end_year = 56; // int
$page_size = 56; // int
$start_key = 'start_key_example'; // string
$start_month = 56; // int
$start_year = 56; // int

try {
    $result = $apiInstance->v1DataCallMonthlySummaryGet($account, $call_type, $end_month, $end_year, $page_size, $start_key, $start_month, $start_year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataCallMonthlySummaryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account** | **string**|  | [optional] |
| **call_type** | **string**|  | [optional] |
| **end_month** | **int**|  | [optional] |
| **end_year** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **start_month** | **int**|  | [optional] |
| **start_year** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallMonthlySummary**](../Model/ServiceDocsCallMonthlySummary.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataEndpointListGet()`

```php
v1DataEndpointListGet($endpoint_name, $feature_name, $page_size, $start_key, $transaction_type, $version): \OpenAPI\Client\Model\ServiceDocsEndpointList
```

Get Endpoint List

Access the endpoint list for each CPaaS API.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$endpoint_name = 'endpoint_name_example'; // string
$feature_name = 'feature_name_example'; // string
$page_size = 56; // int
$start_key = 'start_key_example'; // string
$transaction_type = 'transaction_type_example'; // string
$version = 'version_example'; // string

try {
    $result = $apiInstance->v1DataEndpointListGet($endpoint_name, $feature_name, $page_size, $start_key, $transaction_type, $version);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataEndpointListGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **endpoint_name** | **string**|  | [optional] |
| **feature_name** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **transaction_type** | **string**|  | [optional] |
| **version** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsEndpointList**](../Model/ServiceDocsEndpointList.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataEventDailySummaryGet()`

```php
v1DataEventDailySummaryGet($account_id, $component, $end_date, $page_size, $start_date, $start_key): \OpenAPI\Client\Model\ServiceDocsEventDailySummary
```

Get Event Daily Summary List

Obtain a daily summary of events in a CPaaS account (e.g., setting/resetting the presence status for a user or extension).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$component = 'component_example'; // string
$end_date = 'end_date_example'; // string
$page_size = 56; // int
$start_date = 'start_date_example'; // string
$start_key = 'start_key_example'; // string

try {
    $result = $apiInstance->v1DataEventDailySummaryGet($account_id, $component, $end_date, $page_size, $start_date, $start_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataEventDailySummaryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | [optional] |
| **component** | **string**|  | [optional] |
| **end_date** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_date** | **string**|  | [optional] |
| **start_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsEventDailySummary**](../Model/ServiceDocsEventDailySummary.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataEventDetailGet()`

```php
v1DataEventDetailGet($account_id, $component, $end_date_time, $event_name, $exec_status, $page_size, $start_date_time, $start_key, $username): \OpenAPI\Client\Model\ServiceDocsEventDetail
```

Get Event Details

Obtain specific details about an event (e.g., an E911 notification, a deleted account, or a created user).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$component = 'component_example'; // string
$end_date_time = 'end_date_time_example'; // string
$event_name = 'event_name_example'; // string
$exec_status = 'exec_status_example'; // string
$page_size = 56; // int
$start_date_time = 'start_date_time_example'; // string
$start_key = 'start_key_example'; // string
$username = 'username_example'; // string

try {
    $result = $apiInstance->v1DataEventDetailGet($account_id, $component, $end_date_time, $event_name, $exec_status, $page_size, $start_date_time, $start_key, $username);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataEventDetailGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | [optional] |
| **component** | **string**|  | [optional] |
| **end_date_time** | **string**|  | [optional] |
| **event_name** | **string**|  | [optional] |
| **exec_status** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_date_time** | **string**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **username** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsEventDetail**](../Model/ServiceDocsEventDetail.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataEventMonthlySummaryGet()`

```php
v1DataEventMonthlySummaryGet($account_id, $component, $end_month, $end_year, $page_size, $start_key, $start_month, $start_year): \OpenAPI\Client\Model\ServiceDocsEventMonthlySummary
```

Get Event Monthly Summary List

Obtain a monthly summary of events in a CPaaS account (e.g., adding media files or assigning phone numbers).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$component = 'component_example'; // string
$end_month = 56; // int
$end_year = 56; // int
$page_size = 56; // int
$start_key = 'start_key_example'; // string
$start_month = 56; // int
$start_year = 56; // int

try {
    $result = $apiInstance->v1DataEventMonthlySummaryGet($account_id, $component, $end_month, $end_year, $page_size, $start_key, $start_month, $start_year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataEventMonthlySummaryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | [optional] |
| **component** | **string**|  | [optional] |
| **end_month** | **int**|  | [optional] |
| **end_year** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **start_month** | **int**|  | [optional] |
| **start_year** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsEventMonthlySummary**](../Model/ServiceDocsEventMonthlySummary.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataFeatureDailySummaryGet()`

```php
v1DataFeatureDailySummaryGet($end_date, $feature_name, $page_size, $start_date, $start_key): \OpenAPI\Client\Model\ServiceDocsFeatureDailySummary
```

Get Feature Daily Summary List

Retrieve a daily summary about a feature, including usage, which accounts execute the steps, and other relevant information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$end_date = 'end_date_example'; // string
$feature_name = 'feature_name_example'; // string
$page_size = 56; // int
$start_date = 'start_date_example'; // string
$start_key = 'start_key_example'; // string

try {
    $result = $apiInstance->v1DataFeatureDailySummaryGet($end_date, $feature_name, $page_size, $start_date, $start_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataFeatureDailySummaryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **end_date** | **string**|  | [optional] |
| **feature_name** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_date** | **string**|  | [optional] |
| **start_key** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsFeatureDailySummary**](../Model/ServiceDocsFeatureDailySummary.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1DataFeatureMonthlySummaryGet()`

```php
v1DataFeatureMonthlySummaryGet($end_month, $end_year, $feature_name, $page_size, $start_key, $start_month, $start_year): \OpenAPI\Client\Model\ServiceDocsFeatureMonthlySummary
```

Get Feature Monthly Summary List

Retrieve a monthly summary about a feature’s usage, new users, updates, and other relevant information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DataApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$end_month = 56; // int
$end_year = 56; // int
$feature_name = 'feature_name_example'; // string
$page_size = 56; // int
$start_key = 'start_key_example'; // string
$start_month = 56; // int
$start_year = 56; // int

try {
    $result = $apiInstance->v1DataFeatureMonthlySummaryGet($end_month, $end_year, $feature_name, $page_size, $start_key, $start_month, $start_year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DataApi->v1DataFeatureMonthlySummaryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **end_month** | **int**|  | [optional] |
| **end_year** | **int**|  | [optional] |
| **feature_name** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **start_month** | **int**|  | [optional] |
| **start_year** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsFeatureMonthlySummary**](../Model/ServiceDocsFeatureMonthlySummary.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
