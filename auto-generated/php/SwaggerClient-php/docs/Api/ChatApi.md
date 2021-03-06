# Swagger\Client\ChatApi

All URIs are relative to *https://localhost/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatGet**](ChatApi.md#chatGet) | **GET** /chat | Get chat messages.
[**chatGetChannels**](ChatApi.md#chatGetChannels) | **GET** /chat/channels | Get available channels.
[**chatGetConnected**](ChatApi.md#chatGetConnected) | **GET** /chat/connected | Get connected users.
[**chatNew**](ChatApi.md#chatNew) | **POST** /chat | Send a chat message.


# **chatGet**
> \Swagger\Client\Model\Chat[] chatGet($count, $start, $reverse, $channel_id)

Get chat messages.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\ChatApi();
$count = 100; // float | Number of results to fetch.
$start = 0; // float | Starting point for results.
$reverse = true; // bool | If true, will sort results newest first.
$channel_id = 1.2; // double | Channel id. GET /chat/channels for ids. Leave blank for all.

try {
    $result = $api_instance->chatGet($count, $start, $reverse, $channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->chatGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **count** | **float**| Number of results to fetch. | [optional] [default to 100]
 **start** | **float**| Starting point for results. | [optional] [default to 0]
 **reverse** | **bool**| If true, will sort results newest first. | [optional] [default to true]
 **channel_id** | **double**| Channel id. GET /chat/channels for ids. Leave blank for all. | [optional]

### Return type

[**\Swagger\Client\Model\Chat[]**](../Model/Chat.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml, text/xml, application/javascript, text/javascript

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **chatGetChannels**
> \Swagger\Client\Model\ChatChannel[] chatGetChannels()

Get available channels.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\ChatApi();

try {
    $result = $api_instance->chatGetChannels();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->chatGetChannels: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ChatChannel[]**](../Model/ChatChannel.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml, text/xml, application/javascript, text/javascript

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **chatGetConnected**
> \Swagger\Client\Model\ConnectedUsers chatGetConnected()

Get connected users.

Returns an array with browser users in the first position and API users (bots) in the second position.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\ChatApi();

try {
    $result = $api_instance->chatGetConnected();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->chatGetConnected: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\ConnectedUsers**](../Model/ConnectedUsers.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml, text/xml, application/javascript, text/javascript

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **chatNew**
> \Swagger\Client\Model\Chat chatNew($message, $channel_id)

Send a chat message.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\ChatApi();
$message = "message_example"; // string | 
$channel_id = 1; // double | Channel to post to. Default 1 (English).

try {
    $result = $api_instance->chatNew($message, $channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->chatNew: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message** | **string**|  |
 **channel_id** | **double**| Channel to post to. Default 1 (English). | [optional] [default to 1]

### Return type

[**\Swagger\Client\Model\Chat**](../Model/Chat.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded
 - **Accept**: application/json, application/xml, text/xml, application/javascript, text/javascript

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

