# OpenAPI\Client\CPaaSManagementApi

All URIs are relative to http://api.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1MgmtUserGet()**](CPaaSManagementApi.md#v1MgmtUserGet) | **GET** /v1/mgmt/user | Get All CPaaS Users |
| [**v1MgmtUserPost()**](CPaaSManagementApi.md#v1MgmtUserPost) | **POST** /v1/mgmt/user | Invite CPaaS User |
| [**v1MgmtUserUserIDDelete()**](CPaaSManagementApi.md#v1MgmtUserUserIDDelete) | **DELETE** /v1/mgmt/user/{userID} | Delete CPaaS User |
| [**v1MgmtUserUserIDGet()**](CPaaSManagementApi.md#v1MgmtUserUserIDGet) | **GET** /v1/mgmt/user/{userID} | Get CPaaS User Details |
| [**v1MgmtUserUserIDPut()**](CPaaSManagementApi.md#v1MgmtUserUserIDPut) | **PUT** /v1/mgmt/user/{userID} | Update CPaaS User Role |


## `v1MgmtUserGet()`

```php
v1MgmtUserGet($page_size, $start_key, $sort, $email, $role, $first_name, $last_name): \OpenAPI\Client\Model\ServiceDocsAdminUserGetAll
```

Get All CPaaS Users

Retrieve a list of all CPaaS users in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CPaaSManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_size = 56; // int | number of records to return, range 1 to 100
$start_key = 'start_key_example'; // string | unique to fetch next records
$sort = 'sort_example'; // string | sorting the records by email(default)/role/first_name/last_name, _A is for ascending and _D is for descending, eg: sort=role_A,email_D
$email = 'email_example'; // string | Email
$role = 'role_example'; // string | User Role
$first_name = 'first_name_example'; // string | First Name
$last_name = 'last_name_example'; // string | Last Name

try {
    $result = $apiInstance->v1MgmtUserGet($page_size, $start_key, $sort, $email, $role, $first_name, $last_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CPaaSManagementApi->v1MgmtUserGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_size** | **int**| number of records to return, range 1 to 100 | [optional] |
| **start_key** | **string**| unique to fetch next records | [optional] |
| **sort** | **string**| sorting the records by email(default)/role/first_name/last_name, _A is for ascending and _D is for descending, eg: sort&#x3D;role_A,email_D | [optional] |
| **email** | **string**| Email | [optional] |
| **role** | **string**| User Role | [optional] |
| **first_name** | **string**| First Name | [optional] |
| **last_name** | **string**| Last Name | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAdminUserGetAll**](../Model/ServiceDocsAdminUserGetAll.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1MgmtUserPost()`

```php
v1MgmtUserPost($req_body): \OpenAPI\Client\Model\ServiceDocsAdminUserGetSingle
```

Invite CPaaS User

Link a new CPaaS user to an existing client account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CPaaSManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$req_body = new \OpenAPI\Client\Model\ServiceAdminUserAddData(); // \OpenAPI\Client\Model\ServiceAdminUserAddData | payload fields

try {
    $result = $apiInstance->v1MgmtUserPost($req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CPaaSManagementApi->v1MgmtUserPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **req_body** | [**\OpenAPI\Client\Model\ServiceAdminUserAddData**](../Model/ServiceAdminUserAddData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAdminUserGetSingle**](../Model/ServiceDocsAdminUserGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1MgmtUserUserIDDelete()`

```php
v1MgmtUserUserIDDelete($user_id): \OpenAPI\Client\Model\ServiceDocsAdminUserDelete
```

Delete CPaaS User

Delete a CPaaS user from the associated account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CPaaSManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User ID, numeric

try {
    $result = $apiInstance->v1MgmtUserUserIDDelete($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CPaaSManagementApi->v1MgmtUserUserIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User ID, numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAdminUserDelete**](../Model/ServiceDocsAdminUserDelete.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1MgmtUserUserIDGet()`

```php
v1MgmtUserUserIDGet($user_id): \OpenAPI\Client\Model\ServiceDocsAdminUserGetSingle
```

Get CPaaS User Details

View details about each CPaaS user in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CPaaSManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User ID, numeric

try {
    $result = $apiInstance->v1MgmtUserUserIDGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CPaaSManagementApi->v1MgmtUserUserIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User ID, numeric | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAdminUserGetSingle**](../Model/ServiceDocsAdminUserGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1MgmtUserUserIDPut()`

```php
v1MgmtUserUserIDPut($user_id, $req_body): \OpenAPI\Client\Model\ServiceDocsAdminUserGetSingle
```

Update CPaaS User Role

Update a CPaaS user's role within a client's account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\CPaaSManagementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User ID, numeric
$req_body = new \OpenAPI\Client\Model\ServiceAdminUserEditData(); // \OpenAPI\Client\Model\ServiceAdminUserEditData | payload fields

try {
    $result = $apiInstance->v1MgmtUserUserIDPut($user_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CPaaSManagementApi->v1MgmtUserUserIDPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User ID, numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceAdminUserEditData**](../Model/ServiceAdminUserEditData.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsAdminUserGetSingle**](../Model/ServiceDocsAdminUserGetSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
