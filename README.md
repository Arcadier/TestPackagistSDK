# Arcadier PHP SDK

[![GitHub release](https://img.shields.io/github/v/release/arcadier/testpackagistsdk)](https://img.shields.io/github/v/release/arcadier/testpackagistsdk)

PHP SDK is an API wrapper that allows developers to integrate their PHP applications easily with Arcadier's APIs. The SDK abstracts the API interface into simple function calls by handling the RESTful calls, authentication as well as HTTP parameterisations.

## Requirements
PHP 7.0.0+

## Installation

### Composer
The PHP SDK is hosted on [Packagist](https://packagist.org/packages/arcadier/test-packagist-sdk). First, install composer if you do not have it. Next, to install the SDK, run this command:
```
composer require arcadier/test-packagist-sdk
```


## 💡 Getting Started
1. Install a copy of the SDK into your server
2. Make an API call from a new PHP file

```
require_once '/sdk/ApiSdk.php';

$sdk = new ApiSdk();

$response = $sdk->getAllItems("?maxPrice=75&pageSize=1&pageNumber=1");
```
##  📚 Docs
Our [API documentation](https://apiv2.arcadier.com/?version=latest#68a1094c-77b6-45fb-acc2-aec053d94a28) provides further information on what our API can do as well as the type of responses you will receive from using the functions in the SDK.

## ⚗️ Testing
We provide a test suite to valide the SDK. To start using it, install the SDK-Test Plugin on your admin portal. Create a merchant account and input the merchant id. Click start tests to run the automated test script. The process will take a few seconds to run and will display the test results.