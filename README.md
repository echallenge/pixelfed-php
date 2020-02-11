# Pixelfed PHP Library

PHP Library for [Pixelfed](https://pixelfed.org)

## Installation

Install with [Composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-macos)

```bash
composer require dansup/pixelfed-php
```

## Authentication
To use this library, you must first obtain a Personal Access Token. **Not all instances support this type of authorization yet.**

Navigate to ```/settings/applications``` on the Pixelfed instance and generate a new ```Personal Access Tokens```. Use that token for authentication.


## Examples
### Nodeinfo
```bash
php -f examples/nodeinfo.php
```


## Methods
For a full list of methods, please view the [source code](https://github.com/dansup/pixelfed-php/blob/master/src/PixelfedApi.php). 

### user()
> GET /api/v1/accounts/verify_credentials

**AUTHENTICATION REQUIRED**

```php
use \Pixelfed\PixelfedApi;

$domain = 'https://pixelfed.social';
$token = 'personal-access-token-here';
$api = new PixelfedApi($domain, $token);
$data = $api->user();
```

### accountById($id)
> GET /api/v1/accounts/{$id}

**AUTHENTICATION REQUIRED**

```php
use \Pixelfed\PixelfedApi;

$domain = 'https://pixelfed.social';
$token = 'personal-access-token-here';
$api = new PixelfedApi($domain, $token);
$data = $api->accountById($id);
```

### accountFollowersById($id)
> GET /api/v1/accounts/{$id}/followers

**AUTHENTICATION REQUIRED**

```php
use \Pixelfed\PixelfedApi;

$domain = 'https://pixelfed.social';
$token = 'personal-access-token-here';
$api = new PixelfedApi($domain, $token);
$data = $api->accountFollowersById($id);
```


### accountFollowingById($id)
> GET /api/v1/accounts/{$id}/following

**AUTHENTICATION REQUIRED**

```php
use \Pixelfed\PixelfedApi;

$domain = 'https://pixelfed.social';
$token = 'personal-access-token-here';
$api = new PixelfedApi($domain, $token);
$data = $api->accountFollowingById($id);
```

### nodeinfo()
> GET /api/nodeinfo/2.0.json

```php
use \Pixelfed\PixelfedApi;

$domain = 'https://pixelfed.social';
$api = new PixelfedApi($domain);
$data = $api->nodeinfo();
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Credits

- [Daniel Supernault](https://github.com/dansup)
- [All Contributors](../../contributors)