# DroneClient\UsersApi

All URIs are relative to *http://localhost:8080/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**usersGet**](UsersApi.md#usersGet) | **GET** /users | Get all users
[**usersLoginDelete**](UsersApi.md#usersLoginDelete) | **DELETE** /users/{login} | Delete a user
[**usersLoginGet**](UsersApi.md#usersLoginGet) | **GET** /users/{login} | Get a user
[**usersLoginPatch**](UsersApi.md#usersLoginPatch) | **PATCH** /users/{login} | Update a user
[**usersLoginPost**](UsersApi.md#usersLoginPost) | **POST** /users/{login} | Create a user


# **usersGet**
> \DroneClient\DroneClient\User[] usersGet()

Get all users

Returns all registered, active users in the system.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\UsersApi(new \Http\Adapter\Guzzle6\Client());

try {
    $result = $api_instance->usersGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\DroneClient\DroneClient\User[]**](../Model/User.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **usersLoginDelete**
> usersLoginDelete($login)

Delete a user

Deletes the user with the specified login name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\UsersApi(new \Http\Adapter\Guzzle6\Client());
$login = "login_example"; // string | user login

try {
    $api_instance->usersLoginDelete($login);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersLoginDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login** | **string**| user login |

### Return type

void (empty response body)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **usersLoginGet**
> \DroneClient\DroneClient\User usersLoginGet($login)

Get a user

Returns a user with the specified login name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\UsersApi(new \Http\Adapter\Guzzle6\Client());
$login = "login_example"; // string | user login

try {
    $result = $api_instance->usersLoginGet($login);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersLoginGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login** | **string**| user login |

### Return type

[**\DroneClient\DroneClient\User**](../Model/User.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **usersLoginPatch**
> \DroneClient\DroneClient\User usersLoginPatch($login, $user)

Update a user

Updates an existing user account.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\UsersApi(new \Http\Adapter\Guzzle6\Client());
$login = "login_example"; // string | user login
$user = new \DroneClient\DroneClient\User(); // \DroneClient\DroneClient\User | changes to the user

try {
    $result = $api_instance->usersLoginPatch($login, $user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersLoginPatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login** | **string**| user login |
 **user** | [**\DroneClient\DroneClient\User**](../Model/User.md)| changes to the user |

### Return type

[**\DroneClient\DroneClient\User**](../Model/User.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **usersLoginPost**
> \DroneClient\DroneClient\User usersLoginPost($login)

Create a user

Creates a new user account with the specified external login.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\UsersApi(new \Http\Adapter\Guzzle6\Client());
$login = "login_example"; // string | user login to activate

try {
    $result = $api_instance->usersLoginPost($login);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UsersApi->usersLoginPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login** | **string**| user login to activate |

### Return type

[**\DroneClient\DroneClient\User**](../Model/User.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

