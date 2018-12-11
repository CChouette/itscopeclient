# Swagger\Client\BusinesscartsApi

All URIs are relative to *https://api.itscope.com/2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addLineItem**](BusinesscartsApi.md#addLineItem) | **POST** /business/carts/{cartId}/cartlineitems | Add products to the cart
[**createCart**](BusinesscartsApi.md#createCart) | **POST** /business/carts | Create a cart
[**editCart**](BusinesscartsApi.md#editCart) | **PUT** /business/carts/{cartId} | Edit a cart
[**getCartInfo**](BusinesscartsApi.md#getCartInfo) | **GET** /business/carts/{cartId}/{view}.{type} | Show cart
[**listCarts**](BusinesscartsApi.md#listCarts) | **GET** /business/carts/{view}.{type} | List all carts
[**removeCart**](BusinesscartsApi.md#removeCart) | **DELETE** /business/carts/{cartId} | Remove a cart
[**removeLineItem**](BusinesscartsApi.md#removeLineItem) | **DELETE** /business/carts/{cartId}/cartlineitems/{lineItemId} | Remove products from the cart


# **addLineItem**
> addLineItem($cart_id, $body)

Add products to the cart

Add one or more products with a given quantity to the shopping cart. If no supplier is given, then ITscope will determine your partner supplier with the lowest price.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinesscartsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cart_id = "cart_id_example"; // string | ITscope cart ID. Use \"pool\" to access the pool
$body = new \Swagger\Client\Model\CartLineItemOrderContainer(); // \Swagger\Client\Model\CartLineItemOrderContainer | List of one of the following combinations: Quantity (greater than 0) and: a) ITscope product ID (puid) with an optional supplier ID and optional supplierItemId OR b) supplier ID and supplier item ID. The supplier IDs can be retrieved via GET /company/distributor/, the supplier item ID is the proprietary product number of the supplier.

try {
    $apiInstance->addLineItem($cart_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling BusinesscartsApi->addLineItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cart_id** | **string**| ITscope cart ID. Use \&quot;pool\&quot; to access the pool |
 **body** | [**\Swagger\Client\Model\CartLineItemOrderContainer**](../Model/CartLineItemOrderContainer.md)| List of one of the following combinations: Quantity (greater than 0) and: a) ITscope product ID (puid) with an optional supplier ID and optional supplierItemId OR b) supplier ID and supplier item ID. The supplier IDs can be retrieved via GET /company/distributor/, the supplier item ID is the proprietary product number of the supplier. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, application/json
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createCart**
> createCart($body)

Create a cart

Create a shopping cart with the given name. The cart will be assigned to the user making the request.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinesscartsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\CartOrder(); // \Swagger\Client\Model\CartOrder | The cart's name

try {
    $apiInstance->createCart($body);
} catch (Exception $e) {
    echo 'Exception when calling BusinesscartsApi->createCart: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CartOrder**](../Model/CartOrder.md)| The cart&#39;s name | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, application/json
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **editCart**
> editCart($cart_id, $body)

Edit a cart

Edit a shopping cart. The pool cannot be edited.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinesscartsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cart_id = "cart_id_example"; // string | ITscope cart ID. \"pool\" is not accepted here
$body = new \Swagger\Client\Model\CartOrder(); // \Swagger\Client\Model\CartOrder | The cart's name

try {
    $apiInstance->editCart($cart_id, $body);
} catch (Exception $e) {
    echo 'Exception when calling BusinesscartsApi->editCart: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cart_id** | **string**| ITscope cart ID. \&quot;pool\&quot; is not accepted here |
 **body** | [**\Swagger\Client\Model\CartOrder**](../Model/CartOrder.md)| The cart&#39;s name | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, application/json
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getCartInfo**
> getCartInfo($cart_id, $view, $type)

Show cart

Show basic cart information with cart.xml or cart.json. Show cart line items with cartlineitems.xml or cartlineitems.json.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinesscartsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cart_id = "cart_id_example"; // string | ITscope cart ID. Use \"pool\" to access the pool
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format

try {
    $apiInstance->getCartInfo($cart_id, $view, $type);
} catch (Exception $e) {
    echo 'Exception when calling BusinesscartsApi->getCartInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cart_id** | **string**| ITscope cart ID. Use \&quot;pool\&quot; to access the pool |
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listCarts**
> listCarts($view, $type)

List all carts

List all shopping carts.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinesscartsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$view = "view_example"; // string | View (document)
$type = "type_example"; // string | Output data format

try {
    $apiInstance->listCarts($view, $type);
} catch (Exception $e) {
    echo 'Exception when calling BusinesscartsApi->listCarts: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **view** | **string**| View (document) |
 **type** | **string**| Output data format |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **removeCart**
> removeCart($cart_id)

Remove a cart

Remove a shopping cart and all its line items. The pool cannot be removed.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinesscartsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cart_id = "cart_id_example"; // string | ITscope cart ID. \"pool\" is not accepted here

try {
    $apiInstance->removeCart($cart_id);
} catch (Exception $e) {
    echo 'Exception when calling BusinesscartsApi->removeCart: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cart_id** | **string**| ITscope cart ID. \&quot;pool\&quot; is not accepted here |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, application/json
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **removeLineItem**
> removeLineItem($cart_id, $line_item_id)

Remove products from the cart

Remove a line item from your shopping cart.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BusinesscartsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cart_id = "cart_id_example"; // string | ITscope cart ID. Use \"pool\" to access the pool
$line_item_id = "line_item_id_example"; // string | ITscope shopping cart line item ID

try {
    $apiInstance->removeLineItem($cart_id, $line_item_id);
} catch (Exception $e) {
    echo 'Exception when calling BusinesscartsApi->removeLineItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cart_id** | **string**| ITscope cart ID. Use \&quot;pool\&quot; to access the pool |
 **line_item_id** | **string**| ITscope shopping cart line item ID |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/xml, application/json
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

