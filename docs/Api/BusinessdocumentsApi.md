# Boracomputer\ITScope\BusinessdocumentsApi

All URIs are relative to *https://api.itscope.com/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getDocumentById**](BusinessdocumentsApi.md#getDocumentById) | **GET** /business/documents/{transactionId}/{view}.{type} | Fetch business documents by an ITscope Transaction ID
[**validate**](BusinessdocumentsApi.md#validate) | **POST** /business/documents/validate | Validate order documents in openTRANS v2.1 format semantically
[**validateSchema**](BusinessdocumentsApi.md#validateSchema) | **POST** /business/documents/validateschema | Validate documents in openTRANS V2.1 format against the openTRANS schema


# **getDocumentById**
> getDocumentById($transaction_id, $view, $type)

Fetch business documents by an ITscope Transaction ID

Fetch certain business documents by an ITscope Transaction ID. The current document format is openTRANS 2.1

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Boracomputer\ITScope\Api\BusinessdocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$transaction_id = "transaction_id_example"; // string | ITscope transaction ID
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format

try {
    $apiInstance->getDocumentById($transaction_id, $view, $type);
} catch (Exception $e) {
    echo 'Exception when calling BusinessdocumentsApi->getDocumentById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **transaction_id** | **string**| ITscope transaction ID |
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, text/xml
 - **Accept**: application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **validate**
> validate()

Validate order documents in openTRANS v2.1 format semantically

ORDER documents in the openTRANS v2.1 format can be checked whether they are semantically correct for ITscope.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Boracomputer\ITScope\Api\BusinessdocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->validate();
} catch (Exception $e) {
    echo 'Exception when calling BusinessdocumentsApi->validate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, text/xml
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **validateSchema**
> validateSchema()

Validate documents in openTRANS V2.1 format against the openTRANS schema

Documents of type ORDER, ORDERRESPONSE, DISPATCHNOTIFICATION and INVOICE can be checked whether they are in the valid openTRANS 2.1 format according to the openTRANS schema.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Boracomputer\ITScope\Api\BusinessdocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->validateSchema();
} catch (Exception $e) {
    echo 'Exception when calling BusinessdocumentsApi->validateSchema: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, text/xml
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

