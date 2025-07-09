# OpenAPI\Client\CallQueueMembershipApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDQueuemembershipPost()**](CallQueueMembershipApi.md#v1AccountAccountIDQueuemembershipPost) | **POST** /v1/account/{accountID}/queuemembership | Grant Queue Membership to User |
| [**v1AccountAccountIDQueuemembershipRecipientIDDisablePost()**](CallQueueMembershipApi.md#v1AccountAccountIDQueuemembershipRecipientIDDisablePost) | **POST** /v1/account/{accountID}/queuemembership/{recipientID}/disable | Disable Queue Membership |
| [**v1AccountAccountIDQueuemembershipRecipientIDEnablePost()**](CallQueueMembershipApi.md#v1AccountAccountIDQueuemembershipRecipientIDEnablePost) | **POST** /v1/account/{accountID}/queuemembership/{recipientID}/enable | Enable Queue Membership |


## `v1AccountAccountIDQueuemembershipPost()`

```php
v1AccountAccountIDQueuemembershipPost($account_id, $req_body): \OpenAPI\Client\Model\ServiceDocsQueueMembershipOutput
```

Grant Queue Membership to User

Allow users to create queue memberships for recipients.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueMembershipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPQueueMembershipAddData(); // \OpenAPI\Client\Model\ServiceVOIPQueueMembershipAddData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDQueuemembershipPost($account_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueMembershipApi->v1AccountAccountIDQueuemembershipPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPQueueMembershipAddData**](../Model/ServiceVOIPQueueMembershipAddData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsQueueMembershipOutput**](../Model/ServiceDocsQueueMembershipOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDQueuemembershipRecipientIDDisablePost()`

```php
v1AccountAccountIDQueuemembershipRecipientIDDisablePost($account_id, $recipient_id): \OpenAPI\Client\Model\ServiceAPIResponse
```

Disable Queue Membership

Deactivate queue membership for a recipient.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueMembershipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$recipient_id = 'recipient_id_example'; // string | Recipient ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDQueuemembershipRecipientIDDisablePost($account_id, $recipient_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueMembershipApi->v1AccountAccountIDQueuemembershipRecipientIDDisablePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **recipient_id** | **string**| Recipient ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceAPIResponse**](../Model/ServiceAPIResponse.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDQueuemembershipRecipientIDEnablePost()`

```php
v1AccountAccountIDQueuemembershipRecipientIDEnablePost($account_id, $recipient_id, $req_body): \OpenAPI\Client\Model\ServiceAPIResponse
```

Enable Queue Membership

Activate queue membership for a recipient.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CallQueueMembershipApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$recipient_id = 'recipient_id_example'; // string | Recipient ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPCallQueueEnableMembershipData(); // \OpenAPI\Client\Model\ServiceVOIPCallQueueEnableMembershipData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDQueuemembershipRecipientIDEnablePost($account_id, $recipient_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CallQueueMembershipApi->v1AccountAccountIDQueuemembershipRecipientIDEnablePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **recipient_id** | **string**| Recipient ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPCallQueueEnableMembershipData**](../Model/ServiceVOIPCallQueueEnableMembershipData.md)| payload fields | |

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
