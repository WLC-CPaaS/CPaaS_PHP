# OpenAPI\Client\VoicemailApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountIDVoicemailGet()**](VoicemailApi.md#v1AccountAccountIDVoicemailGet) | **GET** /v1/account/{accountID}/voicemail | Get Voicemail Box List |
| [**v1AccountAccountIDVoicemailPost()**](VoicemailApi.md#v1AccountAccountIDVoicemailPost) | **POST** /v1/account/{accountID}/voicemail | Create Voicemail Box |
| [**v1AccountAccountIDVoicemailVoicemailIDDelete()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDDelete) | **DELETE** /v1/account/{accountID}/voicemail/{voicemailID} | Delete Voicemail Box |
| [**v1AccountAccountIDVoicemailVoicemailIDGet()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDGet) | **GET** /v1/account/{accountID}/voicemail/{voicemailID} | Get Voicemail Box Details |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageGet()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageGet) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message | Get Voicemail Message List |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete) | **DELETE** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Delete Voicemail Message |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Get Voicemail Message Details |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut) | **PUT** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID} | Update Voicemail Message |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet) | **GET** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID}/raw | Get Voicemail Message File |
| [**v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost) | **POST** /v1/account/{accountID}/voicemail/{voicemailID}/message/{messageID}/raw | Add Voicemail Message File |
| [**v1AccountAccountIDVoicemailVoicemailIDMessagePost()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDMessagePost) | **POST** /v1/account/{accountID}/voicemail/{voicemailID}/message | Create Voicemail Message |
| [**v1AccountAccountIDVoicemailVoicemailIDPut()**](VoicemailApi.md#v1AccountAccountIDVoicemailVoicemailIDPut) | **PUT** /v1/account/{accountID}/voicemail/{voicemailID} | Update Voicemail Box |


## `v1AccountAccountIDVoicemailGet()`

```php
v1AccountAccountIDVoicemailGet($account_id, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsVoicemailGetAll
```

Get Voicemail Box List

List all voicemail boxes in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailGet($account_id, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailGetAll**](../Model/ServiceDocsVoicemailGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailPost()`

```php
v1AccountAccountIDVoicemailPost($account_id, $voicemail): \OpenAPI\Client\Model\ServiceDocsVoicemailGetSingle
```

Create Voicemail Box

Create a voicemail box for receiving and storing voicemail messages.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | account ID, 32 alphanumeric
$voicemail = new \OpenAPI\Client\Model\ServiceVOIPVoicemailAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPVoicemailAddEditData | voicemail payload fields

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailPost($account_id, $voicemail);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| account ID, 32 alphanumeric | |
| **voicemail** | [**\OpenAPI\Client\Model\ServiceVOIPVoicemailAddEditData**](../Model/ServiceVOIPVoicemailAddEditData.md)| voicemail payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailGetSingle**](../Model/ServiceDocsVoicemailGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDDelete()`

```php
v1AccountAccountIDVoicemailVoicemailIDDelete($account_id, $voicemail_id): \OpenAPI\Client\Model\ServiceDocsVoicemailGetSingle
```

Delete Voicemail Box

Delete a voicemail box in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$voicemail_id = 'voicemail_id_example'; // string | Voicemail ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDDelete($account_id, $voicemail_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **voicemail_id** | **string**| Voicemail ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailGetSingle**](../Model/ServiceDocsVoicemailGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDGet()`

```php
v1AccountAccountIDVoicemailVoicemailIDGet($account_id, $voicemail_id): \OpenAPI\Client\Model\ServiceDocsVoicemailGetSingle
```

Get Voicemail Box Details

Get information about a single voicemail box.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$voicemail_id = 'voicemail_id_example'; // string | Voicemail ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDGet($account_id, $voicemail_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **voicemail_id** | **string**| Voicemail ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailGetSingle**](../Model/ServiceDocsVoicemailGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDMessageGet()`

```php
v1AccountAccountIDVoicemailVoicemailIDMessageGet($account_id, $voicemail_id, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetAll
```

Get Voicemail Message List

Get a list of voicemail messages from an account's voicemail box.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$voicemail_id = 'voicemail_id_example'; // string | voicemail ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDMessageGet($account_id, $voicemail_id, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDMessageGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **voicemail_id** | **string**| voicemail ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetAll**](../Model/ServiceDocsVoicemailMessageGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete()`

```php
v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete($account_id, $voicemail_id, $message_id): \OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetSingle
```

Delete Voicemail Message

Delete a voicemail message from a voicemail box in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$voicemail_id = 'voicemail_id_example'; // string | Voicemail ID, 32 alpha numeric
$message_id = 'message_id_example'; // string | message ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete($account_id, $voicemail_id, $message_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **voicemail_id** | **string**| Voicemail ID, 32 alpha numeric | |
| **message_id** | **string**| message ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetSingle**](../Model/ServiceDocsVoicemailMessageGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet()`

```php
v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet($account_id, $voicemail_id, $message_id): \OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetSingle
```

Get Voicemail Message Details

Retrieve the container details of an individual voicemail message. This includes a reference to the audio file, but not the message itself.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$voicemail_id = 'voicemail_id_example'; // string | Voicemail ID, 32 alpha numeric
$message_id = 'message_id_example'; // string | Message ID, 39 (yyyymm-<32 id>)

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet($account_id, $voicemail_id, $message_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **voicemail_id** | **string**| Voicemail ID, 32 alpha numeric | |
| **message_id** | **string**| Message ID, 39 (yyyymm-&lt;32 id&gt;) | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetSingle**](../Model/ServiceDocsVoicemailMessageGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut()`

```php
v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut($account_id, $voicemail_id, $message_id, $req_body): \OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetSingle
```

Update Voicemail Message

Copy or move a voicemail message to a different folder in the same voicemail box or move the message to a separate voicemail box.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$voicemail_id = 'voicemail_id_example'; // string | Voicemail ID, 32 alpha numeric
$message_id = 'message_id_example'; // string | Message ID, 39 (yyyymm-<32 id>)
$req_body = new \OpenAPI\Client\Model\ServiceVOIPVoicemailMessageChange(); // \OpenAPI\Client\Model\ServiceVOIPVoicemailMessageChange | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut($account_id, $voicemail_id, $message_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **voicemail_id** | **string**| Voicemail ID, 32 alpha numeric | |
| **message_id** | **string**| Message ID, 39 (yyyymm-&lt;32 id&gt;) | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPVoicemailMessageChange**](../Model/ServiceVOIPVoicemailMessageChange.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetSingle**](../Model/ServiceDocsVoicemailMessageGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet()`

```php
v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet($account_id, $voicemail_id, $message_id): \SplFileObject
```

Get Voicemail Message File

Get the original audio content of a specific voicemail message identified by its unique ID within an account's voicemail box. URL Param \"voicemailID\" is a unique 32-character alphanumeric identifier assigned by the system, which refers to a specific voicemail box. URL Param \"messageID\" is a unique 32-character alphanumeric identifier assigned by the system, which refers to a specific message within a voicemail box.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, unique 32-character alphanumeric identifier
$voicemail_id = 'voicemail_id_example'; // string | Voicemail Box ID, unique 32-character alphanumeric identifier
$message_id = 'message_id_example'; // string | Message ID, unique 32-character alphanumeric identifier

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet($account_id, $voicemail_id, $message_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, unique 32-character alphanumeric identifier | |
| **voicemail_id** | **string**| Voicemail Box ID, unique 32-character alphanumeric identifier | |
| **message_id** | **string**| Message ID, unique 32-character alphanumeric identifier | |

### Return type

**\SplFileObject**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/octet-stream`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost()`

```php
v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost($account_id, $voicemail_id, $message_id, $file): array<string,mixed>
```

Add Voicemail Message File

Associate an audio recording file with the voicemail to fully complete the message.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alphanumeric characters
$voicemail_id = 'voicemail_id_example'; // string | Voicemail ID, 32 alphanumeric characters
$message_id = 'message_id_example'; // string | Message ID, 32 alphanumeric characters
$file = '/path/to/file.txt'; // \SplFileObject | Audio file to upload

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost($account_id, $voicemail_id, $message_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDMessageMessageIDRawPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alphanumeric characters | |
| **voicemail_id** | **string**| Voicemail ID, 32 alphanumeric characters | |
| **message_id** | **string**| Message ID, 32 alphanumeric characters | |
| **file** | **\SplFileObject****\SplFileObject**| Audio file to upload | |

### Return type

**array<string,mixed>**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDMessagePost()`

```php
v1AccountAccountIDVoicemailVoicemailIDMessagePost($account_id, $voicemail_id, $message): \OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetSingle
```

Create Voicemail Message

Create the container information for a recorded voicemail message in a voicemail box.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | account ID, 32 alphanumeric
$voicemail_id = 'voicemail_id_example'; // string | voicemail ID, 32 alphanumeric
$message = new \OpenAPI\Client\Model\ServiceVOIPVoicemailMessageAddData(); // \OpenAPI\Client\Model\ServiceVOIPVoicemailMessageAddData | voicemail message payload fields

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDMessagePost($account_id, $voicemail_id, $message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDMessagePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| account ID, 32 alphanumeric | |
| **voicemail_id** | **string**| voicemail ID, 32 alphanumeric | |
| **message** | [**\OpenAPI\Client\Model\ServiceVOIPVoicemailMessageAddData**](../Model/ServiceVOIPVoicemailMessageAddData.md)| voicemail message payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailMessageGetSingle**](../Model/ServiceDocsVoicemailMessageGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountIDVoicemailVoicemailIDPut()`

```php
v1AccountAccountIDVoicemailVoicemailIDPut($account_id, $voicemail_id, $req_body): \OpenAPI\Client\Model\ServiceDocsVoicemailGetSingle
```

Update Voicemail Box

Update the settings in an individual voicemail box, such as the owner, PIN, etc.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoicemailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$voicemail_id = 'voicemail_id_example'; // string | Voicemail ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceVOIPVoicemailAddEditData(); // \OpenAPI\Client\Model\ServiceVOIPVoicemailAddEditData | payload fields

try {
    $result = $apiInstance->v1AccountAccountIDVoicemailVoicemailIDPut($account_id, $voicemail_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoicemailApi->v1AccountAccountIDVoicemailVoicemailIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **voicemail_id** | **string**| Voicemail ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceVOIPVoicemailAddEditData**](../Model/ServiceVOIPVoicemailAddEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsVoicemailGetSingle**](../Model/ServiceDocsVoicemailGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
