# DroneClient\ReposApi

All URIs are relative to *http://localhost:8080/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**reposOwnerNameDelete**](ReposApi.md#reposOwnerNameDelete) | **DELETE** /repos/{owner}/{name} | Delete a repo
[**reposOwnerNameEncryptPost**](ReposApi.md#reposOwnerNameEncryptPost) | **POST** /repos/{owner}/{name}/encrypt | Encrypt repo secrets
[**reposOwnerNameGet**](ReposApi.md#reposOwnerNameGet) | **GET** /repos/{owner}/{name} | Get a repo
[**reposOwnerNamePatch**](ReposApi.md#reposOwnerNamePatch) | **PATCH** /repos/{owner}/{name} | Updates a repo
[**reposOwnerNamePost**](ReposApi.md#reposOwnerNamePost) | **POST** /repos/{owner}/{name} | Activates a repo


# **reposOwnerNameDelete**
> reposOwnerNameDelete($owner, $name)

Delete a repo

Permanently deletes a repository. It cannot be undone.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\ReposApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository

try {
    $api_instance->reposOwnerNameDelete($owner, $name);
} catch (Exception $e) {
    echo 'Exception when calling ReposApi->reposOwnerNameDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |

### Return type

void (empty response body)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reposOwnerNameEncryptPost**
> reposOwnerNameEncryptPost($owner, $name)

Encrypt repo secrets

Encryptes a Yaml file with secret environment variables for secure public storage.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\ReposApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository

try {
    $api_instance->reposOwnerNameEncryptPost($owner, $name);
} catch (Exception $e) {
    echo 'Exception when calling ReposApi->reposOwnerNameEncryptPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |

### Return type

void (empty response body)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reposOwnerNameGet**
> \DroneClient\DroneClient\Repo reposOwnerNameGet($owner, $name)

Get a repo

Retrieves the details of a repository.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\ReposApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository

try {
    $result = $api_instance->reposOwnerNameGet($owner, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReposApi->reposOwnerNameGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |

### Return type

[**\DroneClient\DroneClient\Repo**](../Model/Repo.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reposOwnerNamePatch**
> \DroneClient\DroneClient\Repo reposOwnerNamePatch($owner, $name, $repo)

Updates a repo

Updates the specified repository.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\ReposApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository
$repo = new \DroneClient\DroneClient\Repo(); // \DroneClient\DroneClient\Repo | The updated repository JSON

try {
    $result = $api_instance->reposOwnerNamePatch($owner, $name, $repo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReposApi->reposOwnerNamePatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |
 **repo** | [**\DroneClient\DroneClient\Repo**](../Model/Repo.md)| The updated repository JSON |

### Return type

[**\DroneClient\DroneClient\Repo**](../Model/Repo.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reposOwnerNamePost**
> \DroneClient\DroneClient\Repo reposOwnerNamePost($owner, $name)

Activates a repo

Activates a repository.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\ReposApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository

try {
    $result = $api_instance->reposOwnerNamePost($owner, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReposApi->reposOwnerNamePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |

### Return type

[**\DroneClient\DroneClient\Repo**](../Model/Repo.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

