<h1 align="center">Arcadier PHP SDK</h1>

<p align="center"> <img style="margin-right: 10px;"src="https://img.shields.io/github/v/release/arcadier/arcadier-php"><img src="https://img.shields.io/packagist/dt/Arcadier/arcadier-php"></p>


* [Introduction]()
* [Requirements](https://github.com/Arcadier/arcadier-php#requirements)
* [How to Install](https://github.com/Arcadier/arcadier-php#installation-via-composer)
* [Getting Started](https://github.com/Arcadier/arcadier-php#-getting-started)
  * [Authentication](https://github.com/Arcadier/arcadier-php#authentication)
  * [Trying it](https://github.com/Arcadier/arcadier-php#trying-it)
* [API Documentation](https://github.com/Arcadier/arcadier-php#-api-documentation)
* [Example Project]()
* [Changelog](https://github.com/Arcadier/arcadier-php#-api-documentation)
* [License](https://github.com/Arcadier/arcadier-php#license)

## Introduction

This PHP SDK is an API wrapper that allows developers to integrate their PHP applications easily with Arcadier's APIs. It does the heavily lifting of building the requests and authentication for every API call

## Requirements
* PHP 7.0.0+
* PHP Server
* An Arcadier marketplace of [package Scale](https://www.arcadier.com/packages.html) or above (including [Enterprise](https://www.arcadier.com/enterprise/))

## Installation via Composer
You can install SDK via composer using the following command line:
```php
composer require arcadier/arcadier-php
```

## 💡 Getting Started
### Authenticating with you marketplace
Once the SDK is installed in your directory, navigate to `arcadier-php/src/.env` and edit the `.env` file by following the instructions in it.

Information you will be required to input:
* CLIENT_ID = ""
* CLIENT_SECRET = ""
* DOMAIN = ""
* PROTOCOL = ""

### Trying it
In every PHP script in your root directory, make sure to include `api.php`
```php
require "vendor\arcadier\arcadier-php\src\api.php";
$sdk = new ApiSdk();
```
Then you will be able to call Arcadier's APIs on your marketplace.

Get your marketplace's information

**GET** **```/api/v2/marketplaces```** is mapped to `$sdk->getMarketplaceInfo();`
```php
$marketplace_info = $sdk->getMarketplaceInfo();
echo $marketplace_info;
```

Listing all items:

**GET** **```/api/v2/items```** is mapped to `$sdk->getAllItems();`
```php
$item_list = $sdk->getAllItems();
echo $item_list['Records']; //The actual array of items is in the "Records" field of the JSON response
```

##  📚 API Documentation
View our full API collection on Postman here: [API documentation](https://apiv2.arcadier.com/).
