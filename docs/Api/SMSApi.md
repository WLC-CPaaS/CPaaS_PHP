# OpenAPI\Client\SMSApi

All URIs are relative to http://api.beta.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1SmsAccountAccountIDCampaignCampaignIDImportGet()**](SMSApi.md#v1SmsAccountAccountIDCampaignCampaignIDImportGet) | **GET** /v1/sms/account/{accountID}/campaign/{campaignID}/import |  |
| [**v1SmsAccountAccountIDCampaignCampaignIDImportPost()**](SMSApi.md#v1SmsAccountAccountIDCampaignCampaignIDImportPost) | **POST** /v1/sms/account/{accountID}/campaign/{campaignID}/import |  |
| [**v1SmsAccountAccountIDCampaignCampaignIDPhonenumberGet()**](SMSApi.md#v1SmsAccountAccountIDCampaignCampaignIDPhonenumberGet) | **GET** /v1/sms/account/{accountID}/campaign/{campaignID}/phonenumber |  |
| [**v1SmsAccountAccountIDCampaignCampaignIDPhonenumberPut()**](SMSApi.md#v1SmsAccountAccountIDCampaignCampaignIDPhonenumberPut) | **PUT** /v1/sms/account/{accountID}/campaign/{campaignID}/phonenumber |  |
| [**v1SmsAccountAccountIDCampaignImportGet()**](SMSApi.md#v1SmsAccountAccountIDCampaignImportGet) | **GET** /v1/sms/account/{accountID}/campaign/import |  |


## `v1SmsAccountAccountIDCampaignCampaignIDImportGet()`

```php
v1SmsAccountAccountIDCampaignCampaignIDImportGet($account_id, $campaign_id): \OpenAPI\Client\Model\ServiceDocsCampaignImportOutput
```



Get details about a single imported campaign in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\SMSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$campaign_id = 'campaign_id_example'; // string | Campaign ID

try {
    $result = $apiInstance->v1SmsAccountAccountIDCampaignCampaignIDImportGet($account_id, $campaign_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SMSApi->v1SmsAccountAccountIDCampaignCampaignIDImportGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **campaign_id** | **string**| Campaign ID | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCampaignImportOutput**](../Model/ServiceDocsCampaignImportOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1SmsAccountAccountIDCampaignCampaignIDImportPost()`

```php
v1SmsAccountAccountIDCampaignCampaignIDImportPost($account_id, $campaign_id): \OpenAPI\Client\Model\ServiceDocsCampaignImportOutput
```



Import campaign

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\SMSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$campaign_id = 'campaign_id_example'; // string | Campaign ID

try {
    $result = $apiInstance->v1SmsAccountAccountIDCampaignCampaignIDImportPost($account_id, $campaign_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SMSApi->v1SmsAccountAccountIDCampaignCampaignIDImportPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **campaign_id** | **string**| Campaign ID | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCampaignImportOutput**](../Model/ServiceDocsCampaignImportOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1SmsAccountAccountIDCampaignCampaignIDPhonenumberGet()`

```php
v1SmsAccountAccountIDCampaignCampaignIDPhonenumberGet($account_id, $campaign_id, $page_num, $page_size): \OpenAPI\Client\Model\ServiceDocsCampaignPhoneNumberOutput
```



Get telephone numbers associated with a campaign.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\SMSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$campaign_id = 'campaign_id_example'; // string | Campaign ID
$page_num = 3.4; // float | Page number
$page_size = 3.4; // float | Page size

try {
    $result = $apiInstance->v1SmsAccountAccountIDCampaignCampaignIDPhonenumberGet($account_id, $campaign_id, $page_num, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SMSApi->v1SmsAccountAccountIDCampaignCampaignIDPhonenumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **campaign_id** | **string**| Campaign ID | |
| **page_num** | **float**| Page number | [optional] |
| **page_size** | **float**| Page size | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCampaignPhoneNumberOutput**](../Model/ServiceDocsCampaignPhoneNumberOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1SmsAccountAccountIDCampaignCampaignIDPhonenumberPut()`

```php
v1SmsAccountAccountIDCampaignCampaignIDPhonenumberPut($account_id, $campaign_id, $req_body): \OpenAPI\Client\Model\ServiceDocsCampaignTagDetagPhonenumbersOutput
```



Associate or dissociate telephone numbers with a campaign.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\SMSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$campaign_id = 'campaign_id_example'; // string | Campaign ID, 32 alpha numeric
$req_body = new \OpenAPI\Client\Model\ServiceCampaignTagDetagPhonenumbers(); // \OpenAPI\Client\Model\ServiceCampaignTagDetagPhonenumbers | payload fields

try {
    $result = $apiInstance->v1SmsAccountAccountIDCampaignCampaignIDPhonenumberPut($account_id, $campaign_id, $req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SMSApi->v1SmsAccountAccountIDCampaignCampaignIDPhonenumberPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **campaign_id** | **string**| Campaign ID, 32 alpha numeric | |
| **req_body** | [**\OpenAPI\Client\Model\ServiceCampaignTagDetagPhonenumbers**](../Model/ServiceCampaignTagDetagPhonenumbers.md)| payload fields | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCampaignTagDetagPhonenumbersOutput**](../Model/ServiceDocsCampaignTagDetagPhonenumbersOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1SmsAccountAccountIDCampaignImportGet()`

```php
v1SmsAccountAccountIDCampaignImportGet($account_id, $page_num, $page_size): \OpenAPI\Client\Model\ServiceDocsCampaignImportedGetAllOutput
```



Get a list of all imported campaigns in an account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\SMSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string | Account ID, 32 alpha numeric
$page_num = 3.4; // float | Page number
$page_size = 3.4; // float | Page size

try {
    $result = $apiInstance->v1SmsAccountAccountIDCampaignImportGet($account_id, $page_num, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SMSApi->v1SmsAccountAccountIDCampaignImportGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**| Account ID, 32 alpha numeric | |
| **page_num** | **float**| Page number | [optional] |
| **page_size** | **float**| Page size | [optional] |

### Return type

[**\OpenAPI\Client\Model\ServiceDocsCampaignImportedGetAllOutput**](../Model/ServiceDocsCampaignImportedGetAllOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
