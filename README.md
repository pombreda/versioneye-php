#a PHP CLI/Library for the VersionEye API

see https://www.versioneye.com/api/v2/swagger_doc.json for API documentation

# WIP dont use it in any way!!!!

##Installation

```
$ composer require "digitalkaoz/versioneye-php" *
```

##Usage

###programmaticly:

```php
<?php

use Rs\VersionEye\Client;

$api = (new Client())->api('services'); // Rs\VersionEye\Api\Api

$api->ping(); //array
```

### cli:

```
$ bin/versioneye services:ping
$ bin/versioneye products:search symfony
```

##TODO

*nearly everything ;) its just a 2h quick hack*

* complete the API
* the Commands are autogenerated of public methods+arguments from the different Api Implementations
* need a clever way for outputting results in a proper format for each api

##CLI Tool

```
$ vendor/bin/box build
$ php versioneye-php.phar
```

##Tests

*follows*