<h1 align="center">Arcadier PHP SDK</h1>

<p align="center"> <img style="margin-right: 10px;"src="https://img.shields.io/github/v/release/arcadier/arcadier-php"><img src="https://img.shields.io/packagist/dt/Arcadier/arcadier-php"></p>


* [Requirements](https://github.com/Arcadier/arcadier-php#requirements)
* [Getting Started](https://github.com/Arcadier/arcadier-php#-getting-started)
* [Documentation for the SDK](https://github.com/Arcadier/arcadier-php#-api-documentation)
* [Documentation for Arcadier's APIs]()
* [Changelog](https://github.com/Arcadier/arcadier-php#-api-documentation)
* [License](https://github.com/Arcadier/arcadier-php#license)

This PHP SDK is an API wrapper that allows developers to integrate their PHP applications easily with Arcadier's APIs. It does the heavily lifting of building the requests and authentication for every API call

## Requirements
* PHP 7.0.0+
* An Arcadier marketplace of [package Scale](https://www.arcadier.com/packages.html) or above (including [Enterprise](https://www.arcadier.com/enterprise/))

## Getting Started
Download the required libraries to your directory using the following Composer command line:
```bash
composer require arcadier/arcadier-php
```

Find the `.env` file in the following directory created: "vendor\arcadier\arcadier-php\src" and replace the variables with the relevant values:
```
CLIENT_ID = ""
CLIENT_SECRET = ""
DOMAIN = ""
PROTOCOL = ""
```

Remember to load the SDK by including the following line in all your PHP scripts:
```php
require "vendor\arcadier\arcadier-php\src\api.php";
$sdk = new ApiSdk(); #this variable does not have to be $sdk, but in this documentation, it will be used throughout
```
---

### Trying it
In every PHP script in your root directory, make sure to include `api.php`
```php
require "vendor\arcadier\arcadier-php\src\api.php";
$sdk = new ApiSdk();
```
Then you will be able to call Arcadier's APIs in your script.

Get your marketplace's information

Endpoint: **GET** **```/api/v2/marketplaces```**
```php
$marketplace_info = $sdk->getMarketplaceInfo();
echo $marketplace_info;
```

Listing all items:

Endpoint: **GET** **```/api/v2/items```**

```php
$item_list = $sdk->getAllItems();
echo $item_list['Records']; //The actual array of items is in the "Records" field of the JSON response
```

## Documentation for the SDK
The full documentation for the SDK can be found [here](https://arcadier.github.io).

## Documentation for APIs
View our full API collection on Postman here: [API documentation](https://apiv2.arcadier.com/).

## Changelog
Our changelog can be accessed [here](https://changelog.arcadier.com/).
