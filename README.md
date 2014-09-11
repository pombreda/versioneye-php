#a PHP CLI/Library for the VersionEye API

see https://www.versioneye.com/api/v2/swagger_doc.json for API documentation

##Installation

```
$ composer require "digitalkaoz/versioneye-php" *
```

##Usage

all API endpoints are implemented, see https://www.versioneye.com/api/ for their docs.


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

##Configuration

to store your generated API Token globally you can create a global config file in your home directory:

`~/.veye.rc` we share the same config file with the ruby cli https://github.com/versioneye/veye

the file would look like:

```rc
:api_key: YOUR_API_TOKEN
```

now you dont have to pass your token on each call
##TODO

* need a clever way for outputting results in a proper format for each api

##CLI Tool

```
$ vendor/bin/box build
$ php versioneye-php.phar
```

##Tests

```
$ vendor/bin/phpspec run
```