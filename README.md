# Arcadier PHP SDK

[![GitHub release](https://img.shields.io/github/v/release/arcadier/testpackagistsdk)](https://img.shields.io/github/v/release/arcadier/testpackagistsdk)

PHP SDK is an API wrapper that allows developers to integrate their PHP applications easily with Arcadier's APIs. The SDK abstracts the API interface into simple function calls by handling the RESTful calls, authentication as well as HTTP parameterisations.

## Requirements
***
PHP 7.0.0+

## Installation
***
The PHP SDK is hosted on [Packagist](https://packagist.org/packages/arcadier/test-packagist-sdk). To install it, run this command: <br />
<code>composer require arcadier/test-packagist-sdk</code>

## 💡 Getting Started
***
1. Install a copy of the SDK into your server
2. Make an API call
<code><br />
require_once '../sdk/ApiSdk.php';

$sdk = new ApiSdk();<br />
$response = $sdk->getAllItems("?maxPrice=75&pageSize=1&pageNumber=1");
<code>