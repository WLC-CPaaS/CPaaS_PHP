# OpenAPI\Client\VoIPUserApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1AccountAccountidUserGet()**](VoIPUserApi.md#v1AccountAccountidUserGet) | **GET** /v1/account/{accountid}/user | Get User List |
| [**v1AccountAccountidUserPost()**](VoIPUserApi.md#v1AccountAccountidUserPost) | **POST** /v1/account/{accountid}/user | Create User |
| [**v1AccountAccountidUserUseridDelete()**](VoIPUserApi.md#v1AccountAccountidUserUseridDelete) | **DELETE** /v1/account/{accountid}/user/{userid} | Delete User |
| [**v1AccountAccountidUserUseridGet()**](VoIPUserApi.md#v1AccountAccountidUserUseridGet) | **GET** /v1/account/{accountid}/user/{userid} | Get User Details |
| [**v1AccountAccountidUserUseridPut()**](VoIPUserApi.md#v1AccountAccountidUserUseridPut) | **PUT** /v1/account/{accountid}/user/{userid} | Update User |
| [**v1AccountAccountidUserUseridUserauthPost()**](VoIPUserApi.md#v1AccountAccountidUserUseridUserauthPost) | **POST** /v1/account/{accountid}/user/{userid}/userauth | Impersonate a User |


## `v1AccountAccountidUserGet()`

```php
v1AccountAccountidUserGet($accountid, $start_key, $page_size): \OpenAPI\Client\Model\ServiceDocsUserGetAll
```

Get User List

Get a list of all VoIP users that includes first and last names, email addresses, extensions, and account statuses.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoIPUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$start_key = 'start_key_example'; // string | start_key for pagination that was returned as next_start_key from your previous call
$page_size = 56; // int | number of records to return, range 1 to 50

try {
    $result = $apiInstance->v1AccountAccountidUserGet($accountid, $start_key, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoIPUserApi->v1AccountAccountidUserGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **start_key** | **string**| start_key for pagination that was returned as next_start_key from your previous call | [optional] |
| **page_size** | **int**| number of records to return, range 1 to 50 | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsUserGetAll**](../Model/ServiceDocsUserGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidUserPost()`

```php
v1AccountAccountidUserPost($accountid, $user): \OpenAPI\Client\Model\ServiceDocsUserGetSingle
```

Create User

Add new users to the account. When a user is added, the system generates their unique 32 alpha numeric ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoIPUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$user = new \OpenAPI\Client\Model\ServiceVOIPUserAdd2(); // \OpenAPI\Client\Model\ServiceVOIPUserAdd2 | user fields

try {
    $result = $apiInstance->v1AccountAccountidUserPost($accountid, $user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoIPUserApi->v1AccountAccountidUserPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **user** | [**\OpenAPI\Client\Model\ServiceVOIPUserAdd2**](../Model/ServiceVOIPUserAdd2.md)| user fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsUserGetSingle**](../Model/ServiceDocsUserGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidUserUseridDelete()`

```php
v1AccountAccountidUserUseridDelete($accountid, $userid): \OpenAPI\Client\Model\ServiceDocsUserGetSingle
```

Delete User

Delete VoIP user access to maintain the security of your accounts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoIPUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$userid = 'userid_example'; // string | User ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidUserUseridDelete($accountid, $userid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoIPUserApi->v1AccountAccountidUserUseridDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **userid** | **string**| User ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsUserGetSingle**](../Model/ServiceDocsUserGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidUserUseridGet()`

```php
v1AccountAccountidUserUseridGet($accountid, $userid): \OpenAPI\Client\Model\ServiceDocsUserGetSingle
```

Get User Details

View specific user details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoIPUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$userid = 'userid_example'; // string | User ID, 32 alpha numeric

try {
    $result = $apiInstance->v1AccountAccountidUserUseridGet($accountid, $userid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoIPUserApi->v1AccountAccountidUserUseridGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **userid** | **string**| User ID, 32 alpha numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsUserGetSingle**](../Model/ServiceDocsUserGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidUserUseridPut()`

```php
v1AccountAccountidUserUseridPut($accountid, $userid, $user): \OpenAPI\Client\Model\ServiceDocsUserGetSingle
```

Update User

Keep user information current. Modify the first and last name, extension, and other pertinent information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoIPUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$userid = 'userid_example'; // string | User ID, 32 alpha numeric
$user = new \OpenAPI\Client\Model\ServiceVOIPUserAdd2(); // \OpenAPI\Client\Model\ServiceVOIPUserAdd2 | user fields

try {
    $result = $apiInstance->v1AccountAccountidUserUseridPut($accountid, $userid, $user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoIPUserApi->v1AccountAccountidUserUseridPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **userid** | **string**| User ID, 32 alpha numeric | |
| **user** | [**\OpenAPI\Client\Model\ServiceVOIPUserAdd2**](../Model/ServiceVOIPUserAdd2.md)| user fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsUserGetSingle**](../Model/ServiceDocsUserGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1AccountAccountidUserUseridUserauthPost()`

```php
v1AccountAccountidUserUseridUserauthPost($accountid, $userid, $user): \OpenAPI\Client\Model\ServiceDocsImpersonateUserGetSingle
```

Impersonate a User

Retrieve a token for making presence calls.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\VoIPUserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountid = 'accountid_example'; // string | Account ID, 32 alpha numeric
$userid = 'userid_example'; // string | User ID, 32 alpha numeric
$user = new \OpenAPI\Client\Model\ServiceVOIPImpersonateUser(); // \OpenAPI\Client\Model\ServiceVOIPImpersonateUser | Payload for impersonate a user

try {
    $result = $apiInstance->v1AccountAccountidUserUseridUserauthPost($accountid, $userid, $user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoIPUserApi->v1AccountAccountidUserUseridUserauthPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountid** | **string**| Account ID, 32 alpha numeric | |
| **userid** | **string**| User ID, 32 alpha numeric | |
| **user** | [**\OpenAPI\Client\Model\ServiceVOIPImpersonateUser**](../Model/ServiceVOIPImpersonateUser.md)| Payload for impersonate a user | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsImpersonateUserGetSingle**](../Model/ServiceDocsImpersonateUserGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
