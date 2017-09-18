# DroneClient\UserApi

All URIs are relative to *http://localhost:8080/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**userGet**](UserApi.md#userGet) | **GET** /user | Gets a user
[**userPatch**](UserApi.md#userPatch) | **PATCH** /user | Updates a user
[**userReposGet**](UserApi.md#userReposGet) | **GET** /user/repos | Get user repos


# **userGet**
> \DroneClient\DroneClient\User userGet()

Gets a user

Returns the currently authenticated user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\UserApi(new \Http\Adapter\Guzzle6\Client());

try {
    $result = $api_instance->userGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\DroneClient\DroneClient\User**](../Model/User.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userPatch**
> \DroneClient\DroneClient\User userPatch($user)

Updates a user

Updates the currently authenticated user.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\UserApi(new \Http\Adapter\Guzzle6\Client());
$user = new \DroneClient\DroneClient\User(); // \DroneClient\DroneClient\User | Updates to the user.

try {
    $result = $api_instance->userPatch($user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userPatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user** | [**\DroneClient\DroneClient\User**](../Model/User.md)| Updates to the user. |

### Return type

[**\DroneClient\DroneClient\User**](../Model/User.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userReposGet**
> \DroneClient\DroneClient\Repo[] userReposGet()

Get user repos

Retrieve the currently authenticated User's Repository list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\UserApi(new \Http\Adapter\Guzzle6\Client());

try {
    $result = $api_instance->userReposGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userReposGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\DroneClient\DroneClient\Repo[]**](../Model/Repo.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

