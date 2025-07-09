# OpenAPI\Client\CallQueueRecipientApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDLoginrecipientRecipientIDPost()**](CallQueueRecipientApi.md#v1AccountAccountIDLoginrecipientRecipientIDPost) | **POST** /v1/account/{accountID}/loginrecipient/{recipientID} | Login as Recipient |
| [**v1AccountAccountIDQueuerecipientGet()**](CallQueueRecipientApi.md#v1AccountAccountIDQueuerecipientGet) | **GET** /v1/account/{accountID}/queuerecipient | Change Recipient Status |
| [**v1AccountAccountIDRecipientRecipientIDStatusPost()**](CallQueueRecipientApi.md#v1AccountAccountIDRecipientRecipientIDStatusPost) | **POST** /v1/account/{accountID}/recipient/{recipientID}/status | Get Recipient List |


## `v1AccountAccountIDLoginrecipientRecipientIDPost()`

```php
v1AccountAccountIDLoginrecipientRecipientIDPost($account_id, $recipient_id, $req_body): \OpenAPI\Client\Model\ServiceDocsCallQueueRecipientLoginLogoutOutput
```

Login as Recipient

Agents must log in to receive calls. Depending on their membership, they can log in to one or more queues. (If an agent is a member of more than one queue, they will receive calls from all the queues they are a part of.)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueRecipientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$recipient_id = 'recipient_id_example'; // string | Recipient ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPCallQueueRecipientLoginLogoutData(); // \OpenAPI\Client\Model\ServiceVOIPCallQueueRecipientLoginLogoutData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDLoginrecipientRecipientIDPost($account_id, $recipient_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueRecipientApi->v1AccountAccountIDLoginrecipientRecipientIDPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **recipient_id** | **string**| Recipient ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPCallQueueRecipientLoginLogoutData**](../Model/ServiceVOIPCallQueueRecipientLoginLogoutData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCallQueueRecipientLoginLogoutOutput**](../Model/ServiceDocsCallQueueRecipientLoginLogoutOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDQueuerecipientGet()`

```php
v1AccountAccountIDQueuerecipientGet($account_id): \OpenAPI\Client\Model\ServiceDocsGetQueueRecipients
```

Change Recipient Status

Get a list of all recipients in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueRecipientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDQueuerecipientGet($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueRecipientApi->v1AccountAccountIDQueuerecipientGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsGetQueueRecipients**](../Model/ServiceDocsGetQueueRecipients.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDRecipientRecipientIDStatusPost()`

```php
v1AccountAccountIDRecipientRecipientIDStatusPost($account_id, $recipient_id, $req_body): \OpenAPI\Client\Model\ServiceAPIResponse
```

Get Recipient List

Change the status of a recipient to ready, away, etc.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueRecipientApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$recipient_id = 'recipient_id_example'; // string | Recipient ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPCallQueueRecipientStatusData(); // \OpenAPI\Client\Model\ServiceVOIPCallQueueRecipientStatusData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDRecipientRecipientIDStatusPost($account_id, $recipient_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueRecipientApi->v1AccountAccountIDRecipientRecipientIDStatusPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **recipient_id** | **string**| Recipient ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPCallQueueRecipientStatusData**](../Model/ServiceVOIPCallQueueRecipientStatusData.md)| payload fields | |

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
