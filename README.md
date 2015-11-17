Yii2 Dadata API client
======================

A PHP library for the DaData.ru REST API

[![Latest Stable Version](https://poser.pugx.org/gietos/yii2-dadata/version)](https://packagist.org/packages/gietos/yii2-dadata)
[![Total Downloads](https://poser.pugx.org/gietos/yii2-dadata/downloads)](https://packagist.org/packages/gietos/yii2-dadata)
[![License](https://poser.pugx.org/gietos/yii2-dadata/license)](https://packagist.org/packages/gietos/yii2-dadata)

[API documentation](https://dadata.ru/api/clean/)

## Installation

The suggested installation method is via [composer](https://getcomposer.org/):

```sh
composer require gietos/yii2-dadata
```

## Usage

In config:

``` php
'components' => [
    // ...
    'dadata' => [
        'class' => '\gietos\yii\Dadata\Client',
        'token' => '...',
        'secret' => '...',
    ],
],
```

Example usage:

``` php
use gietos\yii\Dadata\Client;

/** @var Client $client */
$client = \Yii::$app->dadata;

$address = $client->cleanAddress('msk, tverskaya, 1');
echo 'Result: ' . $address->result . PHP_EOL;
```

[More documentation](https://github.com/gietos/dadata/blob/master/README.md)
