# Swagger\Client\BusinessquotesApi

All URIs are relative to *https://api.itscope.com/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getQuoteByQuoteId**](BusinessquotesApi.md#getQuoteByQuoteId) | **GET** /business/quotes/{quoteId}/{view}.{type} | Fetch a quote by the Tscope quote ID
[**getQuoteList**](BusinessquotesApi.md#getQuoteList) | **GET** /business/quotes/{view}.{type} | Fetch a list of quotes
[**searchQuotes**](BusinessquotesApi.md#searchQuotes) | **GET** /business/quotes/search/{filter}/{view}.{type} | Fetch quotes by filters


# **getQuoteByQuoteId**
> \Swagger\Client\Model\Quote[] getQuoteByQuoteId($quote_id, $view, $type)

Fetch a quote by the Tscope quote ID

Fetch a single quote by the ITscope quote ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinessquotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$quote_id = "quote_id_example"; // string | ITscope quote ID
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format

try {
    $result = $apiInstance->getQuoteByQuoteId($quote_id, $view, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessquotesApi->getQuoteByQuoteId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quote_id** | **string**| ITscope quote ID |
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |

### Return type

[**\Swagger\Client\Model\Quote[]**](../Model/Quote.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getQuoteList**
> \Swagger\Client\Model\Quote[] getQuoteList($view, $type, $sort, $page)

Fetch a list of quotes

Fetch a list of quotes and their statuses

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinessquotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format
$sort = "LAST_MODIFIED"; // string | Sort the results
$page = 1; // int | Large result sets are bundled in multiple pages with 50 results per page.

try {
    $result = $apiInstance->getQuoteList($view, $type, $sort, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessquotesApi->getQuoteList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |
 **sort** | **string**| Sort the results | [optional] [default to LAST_MODIFIED]
 **page** | **int**| Large result sets are bundled in multiple pages with 50 results per page. | [optional] [default to 1]

### Return type

[**\Swagger\Client\Model\Quote[]**](../Model/Quote.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json, text/csv, text/html, application/zip

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **searchQuotes**
> \Swagger\Client\Model\Quote[] searchQuotes($view, $type, $filter, $sort, $page)

Fetch quotes by filters

Search for quotes by using filters

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinessquotesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format
$filter = "filter_example"; // string | Possible criteria are keywords, quoteno, status[DRAFT, PROGRESS, WON, LOST] e.g. quoteno=MAN-20150126-10147 oder status=WON.
$sort = "LAST_MODIFIED"; // string | Sort the results
$page = 1; // int | Large result sets are bundled in multiple pages with 50 results per page.

try {
    $result = $apiInstance->searchQuotes($view, $type, $filter, $sort, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessquotesApi->searchQuotes: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |
 **filter** | **string**| Possible criteria are keywords, quoteno, status[DRAFT, PROGRESS, WON, LOST] e.g. quoteno&#x3D;MAN-20150126-10147 oder status&#x3D;WON. |
 **sort** | **string**| Sort the results | [optional] [default to LAST_MODIFIED]
 **page** | **int**| Large result sets are bundled in multiple pages with 50 results per page. | [optional] [default to 1]

### Return type

[**\Swagger\Client\Model\Quote[]**](../Model/Quote.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json, text/csv, text/html, application/zip

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

