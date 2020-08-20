# Arcadier PHP SDK

[![GitHub release](https://img.shields.io/github/v/release/arcadier/testpackagistsdk)](https://img.shields.io/github/v/release/arcadier/testpackagistsdk)

This PHP SDK is an API wrapper that allows developers to integrate their PHP applications easily with Arcadier's APIs. It does the heavily lifting of building the requests and authentication for every API call.

This lets you focus on **building your front-end** instead of having to worry about if you setup the backend properly with our APIs.

All you need to know is how to which parameters in each function. This is documenteted [here]().

## Requirements
PHP 7.0.0+

## Installation via Composer
You can install SDK via composer using the following command line:
```php
composer require arcadier/test-packagist-sdk
```

## 💡 Getting Started
### Authentication
Once the SDK is installed in your directory, go to `/vendor/arcadier/test-packagist-sdk/sdk/admin_token.php` and `/vendor/arcadier/test-packagist-sdk/sdk/ApiSdk.php` and change the following variables to your marketplace's:

* `$client_id`
* `$client_secret`
* `$marketplace`
* `$protocol` is either https or http depending on your server
* `$marketplace` is your marketplace domain.

`$client_id` and `$client_secret` are found in the Account Settings of you Administrator portal.

### Trying it
In every PHP script you intend to call Arcadier's API, make sure to include the following snippet:
```php
include '../vendor/arcadier/test-packagist-sdk/sdk/ApiSdk.php';
$sdk = new ApiSdk();
```

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

Searching for an item

**POST** **```/api/v2/items```** is mapped to `$sdk->getAllItemsJsonFiltering();`
```php
$data = [
    'keywords' => 'string',
    'pagesize' => 'string',
    'Categories' =>[
        'string'
    ],
    'sellerID' => 'string'
];

$response = $sdk->getAllItemsJsonFiltering($data);
$results = $response['Records']; //The actual array of matching items is in the "Records" field of the JSON response
``

##  📚 API Documentation
View our full API collection on Postman here: [API documentation](https://apiv2.arcadier.com/).