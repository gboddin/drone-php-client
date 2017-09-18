# DroneClient\BuildsApi

All URIs are relative to *http://localhost:8080/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**reposOwnerNameBuildsGet**](BuildsApi.md#reposOwnerNameBuildsGet) | **GET** /repos/{owner}/{name}/builds | Get recent builds
[**reposOwnerNameBuildsNumberGet**](BuildsApi.md#reposOwnerNameBuildsNumberGet) | **GET** /repos/{owner}/{name}/builds/{number} | Get the latest build
[**reposOwnerNameBuildsNumberPost**](BuildsApi.md#reposOwnerNameBuildsNumberPost) | **POST** /repos/{owner}/{name}/builds/{number} | Restart a build
[**reposOwnerNameLogsNumberJobDelete**](BuildsApi.md#reposOwnerNameLogsNumberJobDelete) | **DELETE** /repos/{owner}/{name}/logs/{number}/{job} | Cancel a Job
[**reposOwnerNameLogsNumberJobGet**](BuildsApi.md#reposOwnerNameLogsNumberJobGet) | **GET** /repos/{owner}/{name}/logs/{number}/{job} | Get build logs


# **reposOwnerNameBuildsGet**
> \DroneClient\DroneClient\Build[] reposOwnerNameBuildsGet($owner, $name)

Get recent builds

Returns recent builds for the repository based on name.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\BuildsApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository

try {
    $result = $api_instance->reposOwnerNameBuildsGet($owner, $name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->reposOwnerNameBuildsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |

### Return type

[**\DroneClient\DroneClient\Build[]**](../Model/Build.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reposOwnerNameBuildsNumberGet**
> \DroneClient\DroneClient\Build reposOwnerNameBuildsNumberGet($owner, $name, $number, $branch)

Get the latest build

Returns the latest repository build.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\BuildsApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository
$number = 56; // int | sequential build number
$branch = "branch_example"; // string | name of the branch

try {
    $result = $api_instance->reposOwnerNameBuildsNumberGet($owner, $name, $number, $branch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->reposOwnerNameBuildsNumberGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |
 **number** | **int**| sequential build number |
 **branch** | **string**| name of the branch | [optional]

### Return type

[**\DroneClient\DroneClient\Build**](../Model/Build.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reposOwnerNameBuildsNumberPost**
> \DroneClient\DroneClient\Build reposOwnerNameBuildsNumberPost($owner, $name, $number)

Restart a build

Restart the a build by number.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\BuildsApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository
$number = 56; // int | sequential build number

try {
    $result = $api_instance->reposOwnerNameBuildsNumberPost($owner, $name, $number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->reposOwnerNameBuildsNumberPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |
 **number** | **int**| sequential build number |

### Return type

[**\DroneClient\DroneClient\Build**](../Model/Build.md)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reposOwnerNameLogsNumberJobDelete**
> reposOwnerNameLogsNumberJobDelete($owner, $name, $number, $job)

Cancel a Job

Cancel the a build job by number.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\BuildsApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository
$number = 56; // int | sequential build number
$job = 56; // int | sequential job number

try {
    $api_instance->reposOwnerNameLogsNumberJobDelete($owner, $name, $number, $job);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->reposOwnerNameLogsNumberJobDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |
 **number** | **int**| sequential build number |
 **job** | **int**| sequential job number |

### Return type

void (empty response body)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **reposOwnerNameLogsNumberJobGet**
> reposOwnerNameLogsNumberJobGet($owner, $name, $number, $job)

Get build logs

Returns the build logs for a specific job (build step).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\BuildsApi(new \Http\Adapter\Guzzle6\Client());
$owner = "owner_example"; // string | owner of the repository
$name = "name_example"; // string | name of the repository
$number = 56; // int | sequential build number
$job = 56; // int | sequential job number

try {
    $api_instance->reposOwnerNameLogsNumberJobGet($owner, $name, $number, $job);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->reposOwnerNameLogsNumberJobGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **owner** | **string**| owner of the repository |
 **name** | **string**| name of the repository |
 **number** | **int**| sequential build number |
 **job** | **int**| sequential job number |

### Return type

void (empty response body)

### Authorization

[accessToken](../../README.md#accessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

