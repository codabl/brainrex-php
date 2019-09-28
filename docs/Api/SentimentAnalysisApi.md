# Swagger\Client\SentimentAnalysisApi

All URIs are relative to *https://brainrexapi.appspot.com:5000/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**sentimentGetPriceSentiment**](SentimentAnalysisApi.md#sentimentGetPriceSentiment) | **POST** /get_buy_sentiment | Sentiment analysis score using a model trained for buy signals.
[**sentimentGetSentiment**](SentimentAnalysisApi.md#sentimentGetSentiment) | **POST** /get_sentiment | Sentiment analysis for any given blob of text


# **sentimentGetPriceSentiment**
> string sentimentGetPriceSentiment($text)

Sentiment analysis score using a model trained for buy signals.

Gives a 0 to 1 score, depending on buy/sell sentiment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SentimentAnalysisApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$text = new \Swagger\Client\Model\Text1(); // \Swagger\Client\Model\Text1 | String of text to be analyzed. I can be in any language.

try {
    $result = $apiInstance->sentimentGetPriceSentiment($text);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SentimentAnalysisApi->sentimentGetPriceSentiment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **text** | [**\Swagger\Client\Model\Text1**](../Model/Text1.md)| String of text to be analyzed. I can be in any language. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sentimentGetSentiment**
> string sentimentGetSentiment($text)

Sentiment analysis for any given blob of text

Gives a -1 to 1 score, depending on bearish/bullish sentiment

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SentimentAnalysisApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$text = new \Swagger\Client\Model\Text(); // \Swagger\Client\Model\Text | String of text to be analyzed. I can be in any language.

try {
    $result = $apiInstance->sentimentGetSentiment($text);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SentimentAnalysisApi->sentimentGetSentiment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **text** | [**\Swagger\Client\Model\Text**](../Model/Text.md)| String of text to be analyzed. I can be in any language. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

