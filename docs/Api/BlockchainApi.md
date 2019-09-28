# Swagger\Client\BlockchainApi

All URIs are relative to *https://brainrexapi.appspot.com:5000/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**blockchainAverageTx**](BlockchainApi.md#blockchainAverageTx) | **POST** /average_tx_fee | Calculate average transccion fee of a given blockchain
[**blockchainList**](BlockchainApi.md#blockchainList) | **GET** /list_blockchain | The blockchains data structure supported by the Brainrex API


# **blockchainAverageTx**
> \Swagger\Client\Model\InlineResponse201 blockchainAverageTx($request)

Calculate average transccion fee of a given blockchain

Calculates the average trasnsaction fee of a given

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BlockchainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \Swagger\Client\Model\Request(); // \Swagger\Client\Model\Request | Name of the blockchain and date range.

try {
    $result = $apiInstance->blockchainAverageTx($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BlockchainApi->blockchainAverageTx: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\Request**](../Model/Request.md)| Name of the blockchain and date range. |

### Return type

[**\Swagger\Client\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **blockchainList**
> object[] blockchainList()

The blockchains data structure supported by the Brainrex API

List of supported blockchains networks for analysis. The full history of the networks are available.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\BlockchainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->blockchainList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BlockchainApi->blockchainList: ', $e->getMessage(), PHP_EOL;
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

