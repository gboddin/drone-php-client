# DroneClient
Drone PHP Client

This client was generated from the swagger.yml file.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- Package version: 0.7.3

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), run:

```
composer require gboddin/php-drone-client
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: accessToken
DroneClient\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// DroneClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new DroneClient\Api\BuildsApi();
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

## Documentation for API Endpoints

All URIs are relative to *http://localhost:8080/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BuildsApi* | [**reposOwnerNameBuildsGet**](docs/Api/BuildsApi.md#reposownernamebuildsget) | **GET** /repos/{owner}/{name}/builds | Get recent builds
*BuildsApi* | [**reposOwnerNameBuildsNumberGet**](docs/Api/BuildsApi.md#reposownernamebuildsnumberget) | **GET** /repos/{owner}/{name}/builds/{number} | Get the latest build
*BuildsApi* | [**reposOwnerNameBuildsNumberPost**](docs/Api/BuildsApi.md#reposownernamebuildsnumberpost) | **POST** /repos/{owner}/{name}/builds/{number} | Restart a build
*BuildsApi* | [**reposOwnerNameLogsNumberJobDelete**](docs/Api/BuildsApi.md#reposownernamelogsnumberjobdelete) | **DELETE** /repos/{owner}/{name}/logs/{number}/{job} | Cancel a Job
*BuildsApi* | [**reposOwnerNameLogsNumberJobGet**](docs/Api/BuildsApi.md#reposownernamelogsnumberjobget) | **GET** /repos/{owner}/{name}/logs/{number}/{job} | Get build logs
*ReposApi* | [**reposOwnerNameDelete**](docs/Api/ReposApi.md#reposownernamedelete) | **DELETE** /repos/{owner}/{name} | Delete a repo
*ReposApi* | [**reposOwnerNameEncryptPost**](docs/Api/ReposApi.md#reposownernameencryptpost) | **POST** /repos/{owner}/{name}/encrypt | Encrypt repo secrets
*ReposApi* | [**reposOwnerNameGet**](docs/Api/ReposApi.md#reposownernameget) | **GET** /repos/{owner}/{name} | Get a repo
*ReposApi* | [**reposOwnerNamePatch**](docs/Api/ReposApi.md#reposownernamepatch) | **PATCH** /repos/{owner}/{name} | Updates a repo
*ReposApi* | [**reposOwnerNamePost**](docs/Api/ReposApi.md#reposownernamepost) | **POST** /repos/{owner}/{name} | Activates a repo
*UserApi* | [**userGet**](docs/Api/UserApi.md#userget) | **GET** /user | Gets a user
*UserApi* | [**userPatch**](docs/Api/UserApi.md#userpatch) | **PATCH** /user | Updates a user
*UserApi* | [**userReposGet**](docs/Api/UserApi.md#userreposget) | **GET** /user/repos | Get user repos
*UsersApi* | [**usersGet**](docs/Api/UsersApi.md#usersget) | **GET** /users | Get all users
*UsersApi* | [**usersLoginDelete**](docs/Api/UsersApi.md#userslogindelete) | **DELETE** /users/{login} | Delete a user
*UsersApi* | [**usersLoginGet**](docs/Api/UsersApi.md#usersloginget) | **GET** /users/{login} | Get a user
*UsersApi* | [**usersLoginPatch**](docs/Api/UsersApi.md#usersloginpatch) | **PATCH** /users/{login} | Update a user
*UsersApi* | [**usersLoginPost**](docs/Api/UsersApi.md#usersloginpost) | **POST** /users/{login} | Create a user


## Documentation For Models

 - [Build](docs/Model/Build.md)
 - [BuildStatus](docs/Model/BuildStatus.md)
 - [Feed](docs/Model/Feed.md)
 - [Job](docs/Model/Job.md)
 - [Repo](docs/Model/Repo.md)
 - [User](docs/Model/User.md)


## Documentation For Authorization


## accessToken

- **Type**: API key
- **API key parameter name**: access_token
- **Location**: URL query string


## Author



