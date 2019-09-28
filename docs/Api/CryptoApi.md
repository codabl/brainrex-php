# Swagger\Client\CryptoApi

All URIs are relative to *https://brainrexapi.appspot.com:5000/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**exchangesDownloadCandles**](CryptoApi.md#exchangesDownloadCandles) | **POST** /download_candles | Downloads candle format market data
[**exchangesList**](CryptoApi.md#exchangesList) | **GET** /markets | The markets data structure supported by the Brainrex Market API
[**exchangesMarketmaker**](CryptoApi.md#exchangesMarketmaker) | **POST** /market_making | Market Making as a Service API.
[**exchangesRead**](CryptoApi.md#exchangesRead) | **GET** /exchanges | The exchanges data structure supported by the Brainrex API
[**exchangesTickerDataDownload**](CryptoApi.md#exchangesTickerDataDownload) | **POST** /download_ticker | Download raw ticker data from major crypto markets


# **exchangesDownloadCandles**
> \Swagger\Client\Model\InlineResponse201 exchangesDownloadCandles($request)

Downloads candle format market data

Returns a list of candle data from specified market and data range

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CryptoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \Swagger\Client\Model\Request2(); // \Swagger\Client\Model\Request2 | Person to create

try {
    $result = $apiInstance->exchangesDownloadCandles($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CryptoApi->exchangesDownloadCandles: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\Request2**](../Model/Request2.md)| Person to create |

### Return type

[**\Swagger\Client\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **exchangesList**
> object[] exchangesList()

The markets data structure supported by the Brainrex Market API

Read the list of supported markets ( currency pairs ) in each exchange

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CryptoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->exchangesList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CryptoApi->exchangesList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**object[]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **exchangesMarketmaker**
> \Swagger\Client\Model\InlineResponse2011 exchangesMarketmaker($request)

Market Making as a Service API.

Our AI will trade at the risk level you want, you need to provide your credential to the exchange you are trading at.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CryptoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \Swagger\Client\Model\Request3(); // \Swagger\Client\Model\Request3 | Name of exchange and currency pair you want to provide liquidity

try {
    $result = $apiInstance->exchangesMarketmaker($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CryptoApi->exchangesMarketmaker: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\Request3**](../Model/Request3.md)| Name of exchange and currency pair you want to provide liquidity |

### Return type

[**\Swagger\Client\Model\InlineResponse2011**](../Model/InlineResponse2011.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **exchangesRead**
> object[] exchangesRead()

The exchanges data structure supported by the Brainrex API

Read the list of supported exchanges in the Market Data API

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CryptoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->exchangesRead();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CryptoApi->exchangesRead: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**object[]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **exchangesTickerDataDownload**
> \Swagger\Client\Model\InlineResponse201 exchangesTickerDataDownload($request)

Download raw ticker data from major crypto markets

Downloads specified asset class and market and time frame. Of our raw ticker data format

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CryptoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \Swagger\Client\Model\Request1(); // \Swagger\Client\Model\Request1 | Person to create

try {
    $result = $apiInstance->exchangesTickerDataDownload($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CryptoApi->exchangesTickerDataDownload: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\Request1**](../Model/Request1.md)| Person to create |

### Return type

[**\Swagger\Client\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

