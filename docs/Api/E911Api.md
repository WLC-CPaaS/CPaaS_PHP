# OpenAPI\Client\E911Api

All URIs are relative to http://api.cpaaslabs.net, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1E911Get()**](E911Api.md#v1E911Get) | **GET** /v1/e911 | Get E911 List |
| [**v1E911LocationLocationIDActivatePut()**](E911Api.md#v1E911LocationLocationIDActivatePut) | **PUT** /v1/e911/location/{locationID}/activate | Activate E911 Location |
| [**v1E911LocationLocationIDDelete()**](E911Api.md#v1E911LocationLocationIDDelete) | **DELETE** /v1/e911/location/{locationID} | Delete E911 Location |
| [**v1E911LocationValidatePut()**](E911Api.md#v1E911LocationValidatePut) | **PUT** /v1/e911/location/validate | Validate a Location |
| [**v1E911PhoneNumberDelete()**](E911Api.md#v1E911PhoneNumberDelete) | **DELETE** /v1/e911/{phoneNumber} | Delete E911 Phone Number |
| [**v1E911PhoneNumberLocationActiveGet()**](E911Api.md#v1E911PhoneNumberLocationActiveGet) | **GET** /v1/e911/{phoneNumber}/location/active | Get Actvie Location for a Phone Number |
| [**v1E911PhoneNumberLocationGet()**](E911Api.md#v1E911PhoneNumberLocationGet) | **GET** /v1/e911/{phoneNumber}/location | Get Location List for Phone Number |
| [**v1E911Post()**](E911Api.md#v1E911Post) | **POST** /v1/e911 | Create an E911 Location |


## `v1E911Get()`

```php
v1E911Get(): \OpenAPI\Client\Model\ServiceDocE911URIsApiOutput
```

Get E911 List

Obtain e911 URIs associated with the provided account ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\E911Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->v1E911Get();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling E911Api->v1E911Get: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ServiceDocE911URIsApiOutput**](../Model/ServiceDocE911URIsApiOutput.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1E911LocationLocationIDActivatePut()`

```php
v1E911LocationLocationIDActivatePut($location_id): \OpenAPI\Client\Model\ServiceDocE911ActiveLocationOutput
```

Activate E911 Location

Edit the provision location.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\E911Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$location_id = 'location_id_example'; // string | Location ID

try {
    $result = $apiInstance->v1E911LocationLocationIDActivatePut($location_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling E911Api->v1E911LocationLocationIDActivatePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location_id** | **string**| Location ID | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocE911ActiveLocationOutput**](../Model/ServiceDocE911ActiveLocationOutput.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1E911LocationLocationIDDelete()`

```php
v1E911LocationLocationIDDelete($location_id): \OpenAPI\Client\Model\ServiceDocE911RemoveLocationOutput
```

Delete E911 Location

Remove the location.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\E911Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$location_id = 'location_id_example'; // string | Location ID

try {
    $result = $apiInstance->v1E911LocationLocationIDDelete($location_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling E911Api->v1E911LocationLocationIDDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **location_id** | **string**| Location ID | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocE911RemoveLocationOutput**](../Model/ServiceDocE911RemoveLocationOutput.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1E911LocationValidatePut()`

```php
v1E911LocationValidatePut($req_body): \OpenAPI\Client\Model\ServiceDocE911ValidateLocationOutput
```

Validate a Location

Validate the location details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\E911Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$req_body = new \OpenAPI\Client\Model\ServiceE911ValidateLocationInput(); // \OpenAPI\Client\Model\ServiceE911ValidateLocationInput | location details

try {
    $result = $apiInstance->v1E911LocationValidatePut($req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling E911Api->v1E911LocationValidatePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **req_body** | [**\OpenAPI\Client\Model\ServiceE911ValidateLocationInput**](../Model/ServiceE911ValidateLocationInput.md)| location details | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocE911ValidateLocationOutput**](../Model/ServiceDocE911ValidateLocationOutput.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1E911PhoneNumberDelete()`

```php
v1E911PhoneNumberDelete($phone_number): \OpenAPI\Client\Model\ServiceDocE911RemoveURIApiOutput
```

Delete E911 Phone Number

Delete the e911 URI connected with the account URI.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\E911Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$phone_number = 'phone_number_example'; // string | Phone Number

try {
    $result = $apiInstance->v1E911PhoneNumberDelete($phone_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling E911Api->v1E911PhoneNumberDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phone_number** | **string**| Phone Number | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocE911RemoveURIApiOutput**](../Model/ServiceDocE911RemoveURIApiOutput.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1E911PhoneNumberLocationActiveGet()`

```php
v1E911PhoneNumberLocationActiveGet($phone_number): \OpenAPI\Client\Model\ServiceDocE911ActiveLocationURIApiOutput
```

Get Actvie Location for a Phone Number

Get the e911 location connected with the URI.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\E911Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$phone_number = 'phone_number_example'; // string | Phone Number

try {
    $result = $apiInstance->v1E911PhoneNumberLocationActiveGet($phone_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling E911Api->v1E911PhoneNumberLocationActiveGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phone_number** | **string**| Phone Number | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocE911ActiveLocationURIApiOutput**](../Model/ServiceDocE911ActiveLocationURIApiOutput.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1E911PhoneNumberLocationGet()`

```php
v1E911PhoneNumberLocationGet($phone_number): \OpenAPI\Client\Model\ServiceDocE911LocationsURIApiOutput
```

Get Location List for Phone Number

Access a list of the e911 locations associated with the provided URI.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\E911Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$phone_number = 'phone_number_example'; // string | Phone Number

try {
    $result = $apiInstance->v1E911PhoneNumberLocationGet($phone_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling E911Api->v1E911PhoneNumberLocationGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phone_number** | **string**| Phone Number | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocE911LocationsURIApiOutput**](../Model/ServiceDocE911LocationsURIApiOutput.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1E911Post()`

```php
v1E911Post($req_body): \OpenAPI\Client\Model\ServiceDocE911AddLocationOutput
```

Create an E911 Location

Enter new location details.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\E911Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$req_body = new \OpenAPI\Client\Model\ServiceE911AddLocationInput(); // \OpenAPI\Client\Model\ServiceE911AddLocationInput | location details

try {
    $result = $apiInstance->v1E911Post($req_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling E911Api->v1E911Post: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **req_body** | [**\OpenAPI\Client\Model\ServiceE911AddLocationInput**](../Model/ServiceE911AddLocationInput.md)| location details | |

### Return type

[**\OpenAPI\Client\Model\ServiceDocE911AddLocationOutput**](../Model/ServiceDocE911AddLocationOutput.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
