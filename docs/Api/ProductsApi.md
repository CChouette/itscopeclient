# Swagger\Client\ProductsApi

All URIs are relative to *https://api.itscope.com/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**export**](ProductsApi.md#export) | **GET** /products/exports/{uuid} | Download an export
[**queryDatasheetById**](ProductsApi.md#queryDatasheetById) | **GET** /products/datasheet/id/{itscopeid}/{view}.{type} | Fetch datasheet by ID
[**queryProductByEan**](ProductsApi.md#queryProductByEan) | **GET** /products/ean/{ean}/{view}.{type} | Fetch product by EAN
[**queryProductById**](ProductsApi.md#queryProductById) | **GET** /products/id/{itscopeid}/{view}.{type} | Fetch product by ID
[**queryProductTypes**](ProductsApi.md#queryProductTypes) | **GET** /products/producttypes/{view}.{type} | List of all product types
[**queryProducts**](ProductsApi.md#queryProducts) | **GET** /products/search/{filter}/{view}.{type} | Search products by filter


# **export**
> export($uuid)

Download an export

Download an export via ID, which was defined in ITscope.com.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$uuid = "uuid_example"; // string | ID of the export which should be fetched

try {
    $apiInstance->export($uuid);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->export: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| ID of the export which should be fetched |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip, application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryDatasheetById**
> queryDatasheetById($itscopeid, $view, $type, $language, $accept_language)

Fetch datasheet by ID

Fetch product datasheet by PUID (ITscope product ID)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$itscopeid = "itscopeid_example"; // string | ITscope PUID
$view = "view_example"; // string | View (scope of data)
$type = "type_example"; // string | Output data format
$language = ""; // string | Datasheet language
$accept_language = "de"; // string | Header parameter for the datasheet language

try {
    $apiInstance->queryDatasheetById($itscopeid, $view, $type, $language, $accept_language);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->queryDatasheetById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **itscopeid** | **string**| ITscope PUID |
 **view** | **string**| View (scope of data) |
 **type** | **string**| Output data format |
 **language** | **string**| Datasheet language | [optional] [default to ]
 **accept_language** | **string**| Header parameter for the datasheet language | [optional] [default to de]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/html, application/zip, application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryProductByEan**
> \Swagger\Client\Model\Product[] queryProductByEan($ean, $type, $view, $realtime, $plzproducts, $accept_language)

Fetch product by EAN

Fetch a single product by EAN or UPC. As our catalogue can have multiple products with the same EAN, only the most relevant is returned. To fetch all products, use /products/search.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$ean = "ean_example"; // string | EAN or UPC, example: 0885909565573
$type = "type_example"; // string | Output data format
$view = "view_example"; // string | View (scope of data)
$realtime = false; // bool | Realtime request for all prices
$plzproducts = false; // bool | Items ending with -999, products without ITscope catalogue ID
$accept_language = "de"; // string | Languages of the product content, comma separated (de,en,fr,nl,it,es)

try {
    $result = $apiInstance->queryProductByEan($ean, $type, $view, $realtime, $plzproducts, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->queryProductByEan: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ean** | **string**| EAN or UPC, example: 0885909565573 |
 **type** | **string**| Output data format |
 **view** | **string**| View (scope of data) |
 **realtime** | **bool**| Realtime request for all prices | [optional] [default to false]
 **plzproducts** | **bool**| Items ending with -999, products without ITscope catalogue ID | [optional] [default to false]
 **accept_language** | **string**| Languages of the product content, comma separated (de,en,fr,nl,it,es) | [optional] [default to de]

### Return type

[**\Swagger\Client\Model\Product[]**](../Model/Product.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json, text/csv, text/html, application/zip

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryProductById**
> \Swagger\Client\Model\Product[] queryProductById($itscopeid, $type, $view, $realtime, $accept_language)

Fetch product by ID

Fetch a single product by PUID (ITscope product ID)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$itscopeid = "itscopeid_example"; // string | ITscope PUID
$type = "type_example"; // string | Output data format
$view = "view_example"; // string | View (scope of data)
$realtime = false; // bool | Realtime request for all prices
$accept_language = "de"; // string | Languages of the product content, comma separated (de,en,fr,nl,it,es)

try {
    $result = $apiInstance->queryProductById($itscopeid, $type, $view, $realtime, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->queryProductById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **itscopeid** | **string**| ITscope PUID |
 **type** | **string**| Output data format |
 **view** | **string**| View (scope of data) |
 **realtime** | **bool**| Realtime request for all prices | [optional] [default to false]
 **accept_language** | **string**| Languages of the product content, comma separated (de,en,fr,nl,it,es) | [optional] [default to de]

### Return type

[**\Swagger\Client\Model\Product[]**](../Model/Product.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json, application/zip

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryProductTypes**
> \Swagger\Client\Model\ProductType[] queryProductTypes($type, $view)

List of all product types

A list of all product types for master data mappings.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type = "type_example"; // string | Output data format
$view = "view_example"; // string | View (scope of data)

try {
    $result = $apiInstance->queryProductTypes($type, $view);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->queryProductTypes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **string**| Output data format |
 **view** | **string**| View (scope of data) |

### Return type

[**\Swagger\Client\Model\ProductType[]**](../Model/ProductType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **queryProducts**
> \Swagger\Client\Model\Product[] queryProducts($filter, $type, $view, $realtime, $plzproducts, $page, $item, $sort, $accept_language)

Search products by filter

Fetch single or multiple products, filter and sort them. One or more languages for product content can be specified.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ProductsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$filter = "filter_example"; // string | One or more filter criteria separated by semicolon (AND-search). Within a criteria values can be separated by comma (OR). Possible criteria are ean=0885909565573, distpid=C194570, id=2367755000, keywords=Apple%20Ipad, producttype etc <br> More at the <a href=\"https://support.itscope.com/hc/de/articles/206012542\">Online Help</a>
$type = "type_example"; // string | Output data format
$view = "view_example"; // string | View (scope of data)
$realtime = false; // bool | Realtime request for all prices
$plzproducts = false; // bool | Items ending with -999, products without ITscope catalogue ID
$page = 1; // int | Large result sets are bundled in multiple pages with 50 results per page.
$item = 0; // int | (Not yet implemented) Chooses a single product from the result set and returns only that.
$sort = "DEFAULT"; // string | Sort the results
$accept_language = "de"; // string | Languages of the product content, comma separated (de,en,fr,nl,it,es)

try {
    $result = $apiInstance->queryProducts($filter, $type, $view, $realtime, $plzproducts, $page, $item, $sort, $accept_language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->queryProducts: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **filter** | **string**| One or more filter criteria separated by semicolon (AND-search). Within a criteria values can be separated by comma (OR). Possible criteria are ean&#x3D;0885909565573, distpid&#x3D;C194570, id&#x3D;2367755000, keywords&#x3D;Apple%20Ipad, producttype etc &lt;br&gt; More at the &lt;a href&#x3D;\&quot;https://support.itscope.com/hc/de/articles/206012542\&quot;&gt;Online Help&lt;/a&gt; |
 **type** | **string**| Output data format |
 **view** | **string**| View (scope of data) |
 **realtime** | **bool**| Realtime request for all prices | [optional] [default to false]
 **plzproducts** | **bool**| Items ending with -999, products without ITscope catalogue ID | [optional] [default to false]
 **page** | **int**| Large result sets are bundled in multiple pages with 50 results per page. | [optional] [default to 1]
 **item** | **int**| (Not yet implemented) Chooses a single product from the result set and returns only that. | [optional] [default to 0]
 **sort** | **string**| Sort the results | [optional] [default to DEFAULT]
 **accept_language** | **string**| Languages of the product content, comma separated (de,en,fr,nl,it,es) | [optional] [default to de]

### Return type

[**\Swagger\Client\Model\Product[]**](../Model/Product.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json, text/csv, text/html, application/zip

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

