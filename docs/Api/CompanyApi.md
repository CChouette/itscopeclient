# Swagger\Client\CompanyApi

All URIs are relative to *https://api.itscope.com/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**queryDistributors**](CompanyApi.md#queryDistributors) | **GET** /company/distributor/{view}.{type} | List of all distributors
[**queryManufacturers**](CompanyApi.md#queryManufacturers) | **GET** /company/manufacturer/{view}.{type} | List of all manufacturers


# **queryDistributors**
> \Swagger\Client\Model\Company[] queryDistributors($type, $view)

List of all distributors

A list of all distributors for master data mappings

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CompanyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type = "type_example"; // string | Output data format
$view = "view_example"; // string | View (scope of data)

try {
    $result = $apiInstance->queryDistributors($type, $view);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompanyApi->queryDistributors: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **string**| Output data format |
 **view** | **string**| View (scope of data) |

### Return type

[**\Swagger\Client\Model\Company[]**](../Model/Company.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryManufacturers**
> \Swagger\Client\Model\Company[] queryManufacturers($type, $view)

List of all manufacturers

A liste of all manufacturers for master data mappings

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CompanyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type = "type_example"; // string | Output data format
$view = "view_example"; // string | View (scope of data)

try {
    $result = $apiInstance->queryManufacturers($type, $view);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CompanyApi->queryManufacturers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **string**| Output data format |
 **view** | **string**| View (scope of data) |

### Return type

[**\Swagger\Client\Model\Company[]**](../Model/Company.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

