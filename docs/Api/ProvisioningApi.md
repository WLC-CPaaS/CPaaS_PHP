# OpenAPI\Client\ProvisioningApi

All URIs are relative to http://API_HOSTNAME, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**v1ApBrandBrandFamilyFamilyGet()**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyGet) | **GET** /v1/ap/brand/{brand}/family/{family} | Get Family |
| [**v1ApBrandBrandFamilyFamilyModelGet()**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model | Get Model List |
| [**v1ApBrandBrandFamilyFamilyModelModelGet()**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model} | Get Model |
| [**v1ApBrandBrandFamilyFamilyModelModelTemplateGet()**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelTemplateGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model}/template | Get Template List |
| [**v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet()**](ProvisioningApi.md#v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet) | **GET** /v1/ap/brand/{brand}/family/{family}/model/{model}/template/{template} | Get Template |
| [**v1ApBrandBrandFamilyGet()**](ProvisioningApi.md#v1ApBrandBrandFamilyGet) | **GET** /v1/ap/brand/{brand}/family | Get Family List |
| [**v1ApBrandBrandGet()**](ProvisioningApi.md#v1ApBrandBrandGet) | **GET** /v1/ap/brand/{brand} | Get Brand |
| [**v1ApBrandGet()**](ProvisioningApi.md#v1ApBrandGet) | **GET** /v1/ap/brand | Get Brand |
| [**v1ApConfigfileGeneratePost()**](ProvisioningApi.md#v1ApConfigfileGeneratePost) | **POST** /v1/ap/configfile/generate | Generate config file |


## `v1ApBrandBrandFamilyFamilyGet()`

```php
v1ApBrandBrandFamilyFamilyGet($brand, $family): \OpenAPI\Client\Model\ProvisioningDocsDocsFamilyOutputSingle
```

Get Family

Retrieve a family's details by the randomly generated ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$brand = 'brand_example'; // string | brand
$family = 'family_example'; // string | family

try {
    $result = $apiInstance->v1ApBrandBrandFamilyFamilyGet($brand, $family);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApBrandBrandFamilyFamilyGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **brand** | **string**| brand | |
| **family** | **string**| family | |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsFamilyOutputSingle**](../Model/ProvisioningDocsDocsFamilyOutputSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1ApBrandBrandFamilyFamilyModelGet()`

```php
v1ApBrandBrandFamilyFamilyModelGet($brand, $family, $model_name, $page_size, $start_key, $status): \OpenAPI\Client\Model\ProvisioningDocsDocsModelOutput
```

Get Model List

Retrieve a list of all models within a family for a brand (e.g., Yealink and Polycom).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$brand = 'brand_example'; // string | brand
$family = 'family_example'; // string | family
$model_name = 'model_name_example'; // string
$page_size = 56; // int
$start_key = 'start_key_example'; // string
$status = 'status_example'; // string

try {
    $result = $apiInstance->v1ApBrandBrandFamilyFamilyModelGet($brand, $family, $model_name, $page_size, $start_key, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApBrandBrandFamilyFamilyModelGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **brand** | **string**| brand | |
| **family** | **string**| family | |
| **model_name** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsModelOutput**](../Model/ProvisioningDocsDocsModelOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1ApBrandBrandFamilyFamilyModelModelGet()`

```php
v1ApBrandBrandFamilyFamilyModelModelGet($brand, $family, $model): \OpenAPI\Client\Model\ProvisioningDocsDocsModelOutputSingle
```

Get Model

Retrieve a model's details by the randomly generated ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$brand = 'brand_example'; // string | brand
$family = 'family_example'; // string | family
$model = 'model_example'; // string | model

try {
    $result = $apiInstance->v1ApBrandBrandFamilyFamilyModelModelGet($brand, $family, $model);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApBrandBrandFamilyFamilyModelModelGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **brand** | **string**| brand | |
| **family** | **string**| family | |
| **model** | **string**| model | |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsModelOutputSingle**](../Model/ProvisioningDocsDocsModelOutputSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1ApBrandBrandFamilyFamilyModelModelTemplateGet()`

```php
v1ApBrandBrandFamilyFamilyModelModelTemplateGet($brand, $family, $model, $firmware, $page_size, $start_key, $status, $template_name): \OpenAPI\Client\Model\ProvisioningDocsDocsTemplatesOutput
```

Get Template List

Retrieve a list of all templates for a model within a brand (e.g., Yealink and Polycom).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$brand = 'brand_example'; // string | brand
$family = 'family_example'; // string | family
$model = 'model_example'; // string | model
$firmware = 'firmware_example'; // string
$page_size = 56; // int
$start_key = 'start_key_example'; // string
$status = 'status_example'; // string
$template_name = 'template_name_example'; // string

try {
    $result = $apiInstance->v1ApBrandBrandFamilyFamilyModelModelTemplateGet($brand, $family, $model, $firmware, $page_size, $start_key, $status, $template_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApBrandBrandFamilyFamilyModelModelTemplateGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **brand** | **string**| brand | |
| **family** | **string**| family | |
| **model** | **string**| model | |
| **firmware** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **template_name** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsTemplatesOutput**](../Model/ProvisioningDocsDocsTemplatesOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet()`

```php
v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet($brand, $family, $model, $template): \OpenAPI\Client\Model\ProvisioningDocsDocsTemplateOutputSingle
```

Get Template

Retrieve details about a template for a model by the randomly generated ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$brand = 'brand_example'; // string | brand
$family = 'family_example'; // string | family
$model = 'model_example'; // string | model
$template = 'template_example'; // string | template

try {
    $result = $apiInstance->v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet($brand, $family, $model, $template);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApBrandBrandFamilyFamilyModelModelTemplateTemplateGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **brand** | **string**| brand | |
| **family** | **string**| family | |
| **model** | **string**| model | |
| **template** | **string**| template | |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsTemplateOutputSingle**](../Model/ProvisioningDocsDocsTemplateOutputSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1ApBrandBrandFamilyGet()`

```php
v1ApBrandBrandFamilyGet($brand, $family_name, $page_size, $start_key, $status): \OpenAPI\Client\Model\ProvisioningDocsDocsFamilyOutput
```

Get Family List

Retrieve a list of all families for a brand (e.g., Yealink and Polycom).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$brand = 'brand_example'; // string | brand
$family_name = 'family_name_example'; // string
$page_size = 56; // int
$start_key = 'start_key_example'; // string
$status = 'status_example'; // string

try {
    $result = $apiInstance->v1ApBrandBrandFamilyGet($brand, $family_name, $page_size, $start_key, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApBrandBrandFamilyGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **brand** | **string**| brand | |
| **family_name** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsFamilyOutput**](../Model/ProvisioningDocsDocsFamilyOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1ApBrandBrandGet()`

```php
v1ApBrandBrandGet($brand): \OpenAPI\Client\Model\ProvisioningDocsDocsBrandOutputSingle
```

Get Brand

Retrieve a brand's details by the randomly generated ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$brand = 'brand_example'; // string | brand id to retrieve a brand

try {
    $result = $apiInstance->v1ApBrandBrandGet($brand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApBrandBrandGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **brand** | **string**| brand id to retrieve a brand | |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsBrandOutputSingle**](../Model/ProvisioningDocsDocsBrandOutputSingle.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1ApBrandGet()`

```php
v1ApBrandGet($brand_name, $page_size, $start_key, $status): \OpenAPI\Client\Model\ProvisioningDocsDocsBrandsOutput
```

Get Brand

Retrieve a list of all brands (e.g., Yealink and Polycom) by client.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$brand_name = 'brand_name_example'; // string
$page_size = 56; // int
$start_key = 'start_key_example'; // string
$status = 'status_example'; // string

try {
    $result = $apiInstance->v1ApBrandGet($brand_name, $page_size, $start_key, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApBrandGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **brand_name** | **string**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **start_key** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsBrandsOutput**](../Model/ProvisioningDocsDocsBrandsOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `v1ApConfigfileGeneratePost()`

```php
v1ApConfigfileGeneratePost($params): \OpenAPI\Client\Model\ProvisioningDocsDocsConfigFileOutput
```

Generate config file

Generate a configuration file that includes a list of parameters passed to the specified template_id in the request payload, with populated values returned in the response.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: BearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\ProvisioningApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$params = new \OpenAPI\Client\Model\ModelsGenerateConfigFileRequest(); // \OpenAPI\Client\Model\ModelsGenerateConfigFileRequest | body params to generate config file

try {
    $result = $apiInstance->v1ApConfigfileGeneratePost($params);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvisioningApi->v1ApConfigfileGeneratePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **params** | [**\OpenAPI\Client\Model\ModelsGenerateConfigFileRequest**](../Model/ModelsGenerateConfigFileRequest.md)| body params to generate config file | |

### Return type

[**\OpenAPI\Client\Model\ProvisioningDocsDocsConfigFileOutput**](../Model/ProvisioningDocsDocsConfigFileOutput.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
