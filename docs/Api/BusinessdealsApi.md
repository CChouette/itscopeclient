# Swagger\Client\BusinessdealsApi

All URIs are relative to *https://api.itscope.com/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**archiveDeal**](BusinessdealsApi.md#archiveDeal) | **PUT** /business/deals/archive/{dealId} | Archive order
[**getDealByOrderId**](BusinessdealsApi.md#getDealByOrderId) | **GET** /business/deals/{dealId}/{view}.{type} | Fetch an order by the ITscope order ID
[**getDealList**](BusinessdealsApi.md#getDealList) | **GET** /business/deals/{view}.{type} | Fetch list of orders
[**newDeal**](BusinessdealsApi.md#newDeal) | **POST** /business/deals/send/{distributorId} | Send a new order via ITscope
[**searchDeals**](BusinessdealsApi.md#searchDeals) | **GET** /business/deals/search/{filter}/{view}.{type} | Search orders with filters


# **archiveDeal**
> archiveDeal($deal_id)

Archive order

Archive order by order ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinessdealsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$deal_id = "deal_id_example"; // string | ITscope order ID

try {
    $apiInstance->archiveDeal($deal_id);
} catch (Exception $e) {
    echo 'Exception when calling BusinessdealsApi->archiveDeal: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deal_id** | **string**| ITscope order ID |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, text/xml
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDealByOrderId**
> \Swagger\Client\Model\Deal[] getDealByOrderId($deal_id, $view, $type)

Fetch an order by the ITscope order ID

Fetch single orders by ITscope order ID. Links to the corresponding openTRANS 2.1 documents are in the response.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinessdealsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$deal_id = "deal_id_example"; // string | ITscope order ID
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format

try {
    $result = $apiInstance->getDealByOrderId($deal_id, $view, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessdealsApi->getDealByOrderId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deal_id** | **string**| ITscope order ID |
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |

### Return type

[**\Swagger\Client\Model\Deal[]**](../Model/Deal.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, text/xml
 - **Accept**: application/xml, application/json, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getDealList**
> \Swagger\Client\Model\Deal[] getDealList($view, $type, $archiv, $business_type, $sort, $page)

Fetch list of orders

Fetch a list of orders and their statuses

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinessdealsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format
$archiv = "ALL"; // string | Filter for the archive flag: ARCHIVED: archived, NOTARCHIVED: not archived and ALL: All orders
$business_type = "PURCHASE"; // string | Filter for the business type: PURCHASE: outgoing deals, for sellers - SALE: ingoing deals, for resellers
$sort = "LAST_MODIFIED"; // string | Sort the received orders
$page = 1; // int | Large result sets are bundled in multiple pages with 50 results per page.

try {
    $result = $apiInstance->getDealList($view, $type, $archiv, $business_type, $sort, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessdealsApi->getDealList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |
 **archiv** | **string**| Filter for the archive flag: ARCHIVED: archived, NOTARCHIVED: not archived and ALL: All orders | [optional] [default to ALL]
 **business_type** | **string**| Filter for the business type: PURCHASE: outgoing deals, for sellers - SALE: ingoing deals, for resellers | [optional] [default to PURCHASE]
 **sort** | **string**| Sort the received orders | [optional] [default to LAST_MODIFIED]
 **page** | **int**| Large result sets are bundled in multiple pages with 50 results per page. | [optional] [default to 1]

### Return type

[**\Swagger\Client\Model\Deal[]**](../Model/Deal.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, text/xml
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **newDeal**
> newDeal($distributor_id)

Send a new order via ITscope

Send a new order in valid openTRANS 2.1 format via ITscope to a distributor

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinessdealsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$distributor_id = "distributor_id_example"; // string | ITscope distributor ID

try {
    $apiInstance->newDeal($distributor_id);
} catch (Exception $e) {
    echo 'Exception when calling BusinessdealsApi->newDeal: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **distributor_id** | **string**| ITscope distributor ID |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, text/xml
 - **Accept**: application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **searchDeals**
> \Swagger\Client\Model\Deal[] searchDeals($view, $type, $filter, $archiv, $business_type, $sort, $page)

Search orders with filters

Search orders with filters

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinessdealsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format
$filter = "filter_example"; // string | Possible criteria are keywords, dealId, customerDealId, cartId e.g. dealId=11SRRK-150126-1136.
$archiv = "ALL"; // string | Filter for the archive flag: ARCHIVED: archived, NOTARCHIVED: not archived and ALL: All orders
$business_type = "PURCHASE"; // string | Filter for the business type: PURCHASE: outgoing deals, for sellers - SALE: ingoing deals, for resellers
$sort = "LAST_MODIFIED"; // string | Sort the received orders
$page = 1; // int | Large result sets are bundled in multiple pages with 50 results per page.

try {
    $result = $apiInstance->searchDeals($view, $type, $filter, $archiv, $business_type, $sort, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BusinessdealsApi->searchDeals: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |
 **filter** | **string**| Possible criteria are keywords, dealId, customerDealId, cartId e.g. dealId&#x3D;11SRRK-150126-1136. |
 **archiv** | **string**| Filter for the archive flag: ARCHIVED: archived, NOTARCHIVED: not archived and ALL: All orders | [optional] [default to ALL]
 **business_type** | **string**| Filter for the business type: PURCHASE: outgoing deals, for sellers - SALE: ingoing deals, for resellers | [optional] [default to PURCHASE]
 **sort** | **string**| Sort the received orders | [optional] [default to LAST_MODIFIED]
 **page** | **int**| Large result sets are bundled in multiple pages with 50 results per page. | [optional] [default to 1]

### Return type

[**\Swagger\Client\Model\Deal[]**](../Model/Deal.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

