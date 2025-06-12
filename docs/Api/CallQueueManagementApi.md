# OpenAPI\Client\CallQueueManagementApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDCallqueueGet()**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueGet) | **GET** /v1/account/{accountID}/callqueue | Get Call Queues |
| [**v1AccountAccountIDCallqueuePost()**](CallQueueManagementApi.md#v1AccountAccountIDCallqueuePost) | **POST** /v1/account/{accountID}/callqueue | Create Call Queue |
| [**v1AccountAccountIDCallqueueQueueIDDelete()**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueQueueIDDelete) | **DELETE** /v1/account/{accountID}/callqueue/{queueID} | Delete Call Queue |
| [**v1AccountAccountIDCallqueueQueueIDGet()**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueQueueIDGet) | **GET** /v1/account/{accountID}/callqueue/{queueID} | Get Call Queue Details |
| [**v1AccountAccountIDCallqueueQueueIDPut()**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueQueueIDPut) | **PUT** /v1/account/{accountID}/callqueue/{queueID} | Update Call Queue |
| [**v1AccountAccountIDCallqueueQueueIDStatusGet()**](CallQueueManagementApi.md#v1AccountAccountIDCallqueueQueueIDStatusGet) | **GET** /v1/account/{accountID}/callqueue/{queueID}/status | Get Call Queue Status |
| [**v1AccountAccountIDQueuerolesGet()**](CallQueueManagementApi.md#v1AccountAccountIDQueuerolesGet) | **GET** /v1/account/{accountID}/queueroles | Get Queue Roles of Account |
| [**v1AccountAccountIDQueuerolesQueueIDPost()**](CallQueueManagementApi.md#v1AccountAccountIDQueuerolesQueueIDPost) | **POST** /v1/account/{accountID}/queueroles/{queueID} | Assign Queue Role to Call Queue |


## `v1AccountAccountIDCallqueueGet()`

```php
v1AccountAccountIDCallqueueGet($account_id): \OpenAPI\Client\Model\ServiceDocsCallQueueGetAll
```

Get Call Queues

Retrieve call queue details for an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDCallqueueGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueManagementApi->v1AccountAccountIDCallqueueGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallQueueGetAll**](../Model/ServiceDocsCallQueueGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallqueuePost()`

```php
v1AccountAccountIDCallqueuePost($account_id, $req_body): \OpenAPI\Client\Model\ServiceDocsCallQueueGetSingle
```

Create Call Queue

Set up a call queue in an account for specific inbound calls.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPCallQueueAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPCallQueueAddEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDCallqueuePost($account_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueManagementApi->v1AccountAccountIDCallqueuePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPCallQueueAddEditData**](../Model/ServiceVOIPCallQueueAddEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallQueueGetSingle**](../Model/ServiceDocsCallQueueGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallqueueQueueIDDelete()`

```php
v1AccountAccountIDCallqueueQueueIDDelete($account_id, $queue_id): \OpenAPI\Client\Model\ServiceDocsCallQueueGetSingle
```

Delete Call Queue

Remove the call queue from an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$queue_id = 'queue_id_example'; // string | Queue ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDCallqueueQueueIDDelete($account_id, $queue_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueManagementApi->v1AccountAccountIDCallqueueQueueIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **queue_id** | **string**| Queue ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallQueueGetSingle**](../Model/ServiceDocsCallQueueGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallqueueQueueIDGet()`

```php
v1AccountAccountIDCallqueueQueueIDGet($account_id, $queue_id): \OpenAPI\Client\Model\ServiceDocsCallQueueGetSingle
```

Get Call Queue Details

Capture metadata about a specific queue, such as queue_type and agent_wrapup_time.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$queue_id = 'queue_id_example'; // string | Queue ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDCallqueueQueueIDGet($account_id, $queue_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueManagementApi->v1AccountAccountIDCallqueueQueueIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **queue_id** | **string**| Queue ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallQueueGetSingle**](../Model/ServiceDocsCallQueueGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallqueueQueueIDPut()`

```php
v1AccountAccountIDCallqueueQueueIDPut($account_id, $queue_id, $req_body): \OpenAPI\Client\Model\ServiceDocsCallQueueGetSingle
```

Update Call Queue

Update the metadata mentioned above.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$queue_id = 'queue_id_example'; // string | Queue ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPCallQueueAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPCallQueueAddEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDCallqueueQueueIDPut($account_id, $queue_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueManagementApi->v1AccountAccountIDCallqueueQueueIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **queue_id** | **string**| Queue ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPCallQueueAddEditData**](../Model/ServiceVOIPCallQueueAddEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallQueueGetSingle**](../Model/ServiceDocsCallQueueGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDCallqueueQueueIDStatusGet()`

```php
v1AccountAccountIDCallqueueQueueIDStatusGet($account_id, $queue_id): \OpenAPI\Client\Model\ServiceDocsCallQueueGetSingleStatus
```

Get Call Queue Status

Access the status of a call queue in an account, such as the number of available agents (recipients), estimated wait time, and number of active sessions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$queue_id = 'queue_id_example'; // string | Queue ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDCallqueueQueueIDStatusGet($account_id, $queue_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueManagementApi->v1AccountAccountIDCallqueueQueueIDStatusGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **queue_id** | **string**| Queue ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallQueueGetSingleStatus**](../Model/ServiceDocsCallQueueGetSingleStatus.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDQueuerolesGet()`

```php
v1AccountAccountIDQueuerolesGet($account_id): \OpenAPI\Client\Model\ServiceDocsCallQueueGetRoles
```

Get Queue Roles of Account

Obtain data about each queue role in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDQueuerolesGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueManagementApi->v1AccountAccountIDQueuerolesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallQueueGetRoles**](../Model/ServiceDocsCallQueueGetRoles.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDQueuerolesQueueIDPost()`

```php
v1AccountAccountIDQueuerolesQueueIDPost($account_id, $queue_id, $req_body): \OpenAPI\Client\Model\ServiceAPIResponse
```

Assign Queue Role to Call Queue

Assign roles to members in a call queue.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$queue_id = 'queue_id_example'; // string | Queue ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPCallQueueRoleAssignData(); // \OpenAPI\Client\Model\ServiceVOIPCallQueueRoleAssignData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDQueuerolesQueueIDPost($account_id, $queue_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueManagementApi->v1AccountAccountIDQueuerolesQueueIDPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **queue_id** | **string**| Queue ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPCallQueueRoleAssignData**](../Model/ServiceVOIPCallQueueRoleAssignData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceAPIResponse**](../Model/ServiceAPIResponse.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
