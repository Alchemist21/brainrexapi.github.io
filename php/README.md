# SwaggerClient-php
Welcome to the Brainrex API. We offered pre-trained ML models tackling problems such as Sentiment Analysis, Face ID recognition making, blockchain monitoring and real-tie face-id verification. This AI models can be consumed from this API. You can integrate with your programming language of choice through our [Client Libraries](clients.md) .We also offer integrations to open data and propietary data providers. There is a collection of data transformation tools. Join our Telegram group to get the latest news and ask us questions directly (https://t.me/brainrex). More about Brainrex at [https://brainrex.com](http://brainrex.com). Full Documentation can be found at [https://developers.brainrex.com](https://brainrexapi.github.io/docs)

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 0.1.6
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
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

$apiInstance = new Swagger\Client\Api\BlockchainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->blockchainGetEthereumPrice();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BlockchainApi->blockchainGetEthereumPrice: ', $e->getMessage(), PHP_EOL;
}

$apiInstance = new Swagger\Client\Api\BlockchainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->blockchainGetEthereumSupply();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BlockchainApi->blockchainGetEthereumSupply: ', $e->getMessage(), PHP_EOL;
}

$apiInstance = new Swagger\Client\Api\BlockchainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->blockchainListBlockchains();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BlockchainApi->blockchainListBlockchains: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://brainrexapi.appspot.com/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BlockchainApi* | [**blockchainGetEthereumPrice**](docs/Api/BlockchainApi.md#blockchaingetethereumprice) | **GET** /get_price_ | Lastest price quote for Ether
*BlockchainApi* | [**blockchainGetEthereumSupply**](docs/Api/BlockchainApi.md#blockchaingetethereumsupply) | **GET** /get_ethereum_supply | Total Supply of Ether
*BlockchainApi* | [**blockchainListBlockchains**](docs/Api/BlockchainApi.md#blockchainlistblockchains) | **GET** /list_blockchain | The blockchains data structure supported by the Brainrex API
*CryptoApi* | [**cryptoDownloadCandles**](docs/Api/CryptoApi.md#cryptodownloadcandles) | **POST** /download_candles | Downloads candle format market data
*CryptoApi* | [**cryptoListExchanges**](docs/Api/CryptoApi.md#cryptolistexchanges) | **GET** /exchanges | Available exchanges for the Brainrex Data
*CryptoApi* | [**cryptoListMarkets**](docs/Api/CryptoApi.md#cryptolistmarkets) | **GET** /markets | The markets data structure supported by the Brainrex Market API
*CryptoApi* | [**cryptoTickerDataDownload**](docs/Api/CryptoApi.md#cryptotickerdatadownload) | **POST** /download_ticker | Download raw ticker data from major crypto markets
*CryptoLanguageApi* | [**sentimentGetCryptoSentiment**](docs/Api/CryptoLanguageApi.md#sentimentgetcryptosentiment) | **POST** /crypto_sentiment | Sentiment that reacts to crypto price changes and blockchain events e.g hard forks, chain splits.
*CryptoLanguageApi* | [**sentimentGetEntities**](docs/Api/CryptoLanguageApi.md#sentimentgetentities) | **POST** /get_entities | General Sentiment Analysis scoring
*CryptoLanguageApi* | [**sentimentGetEntitiesSentiment**](docs/Api/CryptoLanguageApi.md#sentimentgetentitiessentiment) | **POST** /get_entities_sentiment | Gets entities and the sentiment for each entity, as well as the importance they have towards the sentiment of the general sentiment
*CryptoLanguageApi* | [**sentimentGetSentimentScore**](docs/Api/CryptoLanguageApi.md#sentimentgetsentimentscore) | **POST** /general_sentiment | General Sentiment Analysis scoring
*FaceIDApi* | [**faceidExtractFace**](docs/Api/FaceIDApi.md#faceidextractface) | **POST** /extract_face | Extracts and validates photo id for passports
*FaceIDApi* | [**faceidExtractMrz**](docs/Api/FaceIDApi.md#faceidextractmrz) | **POST** /extract_mrz | Extracts and validates Machine Readable Zones for passports
*FaceIDApi* | [**faceidFaceMatching**](docs/Api/FaceIDApi.md#faceidfacematching) | **POST** /verify_face | Matches the Face extracted from passport to a selfie uploaded by client
*LibraApi* | [**getLibraStats**](docs/Api/LibraApi.md#getlibrastats) | **GET** /get_libraStats/{byDays} | Info for a specific pet

## Documentation For Models

 - [Body](docs/Model/Body.md)
 - [Body1](docs/Model/Body1.md)
 - [Body2](docs/Model/Body2.md)
 - [Body3](docs/Model/Body3.md)
 - [Body4](docs/Model/Body4.md)
 - [Body5](docs/Model/Body5.md)
 - [Body6](docs/Model/Body6.md)
 - [Body7](docs/Model/Body7.md)
 - [Body8](docs/Model/Body8.md)
 - [Entities](docs/Model/Entities.md)
 - [Entity](docs/Model/Entity.md)
 - [Error](docs/Model/Error.md)
 - [LibraStats](docs/Model/LibraStats.md)
 - [Libras](docs/Model/Libras.md)
 - [MRZ](docs/Model/MRZ.md)
 - [OHCLV](docs/Model/OHCLV.md)
 - [Sentiment](docs/Model/Sentiment.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author

hello@brainrex.com
