# Flysystem adapter for fallback filesystems

[![Build Status](https://img.shields.io/travis/jenszahner/flysystem-fallback-adapter/master.svg?style=flat-square)](https://travis-ci.org/jenszahner/flysystem-fallback-adapter)
[![Coverage Status](https://img.shields.io/scrutinizer/coverage/g/jenszahner/flysystem-fallback-adapter.svg?style=flat-square)](https://scrutinizer-ci.com/g/jenszahner/flysystem-fallback-adapter/code-structure)
[![Quality Score](https://img.shields.io/scrutinizer/g/litipk/flysystem-fallback-adapter.svg?style=flat-square)](https://scrutinizer-ci.com/g/jenszahner/flysystem-fallback-adapter)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Packagist Version](https://img.shields.io/packagist/v/litipk/flysystem-fallback-adapter.svg?style=flat-square)](https://packagist.org/packages/jenszahner/flysystem-fallback-adapter)
[![Total Downloads](https://img.shields.io/packagist/dt/litipk/flysystem-fallback-adapter.svg?style=flat-square)](https://packagist.org/packages/jenszahner/flysystem-fallback-adapter)


This adapter has been created to allow using a fallback filesystem for read operations when the files can't be accessed
through the main adapter.


## Installation

```bash
composer require jenszahner/flysystem-fallback-adapter
```

## Usage

```php
$main = new League\Flysystem\Adapter\AwsS3(...);
$fallback = new League\Flysystem\Adapter\Local(...);
$adapter = new Litipk\Flysystem\Fallback\FallbackAdapter($main, $fallback);
```
