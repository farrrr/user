# Konekt User

[![Travis Build Status](https://img.shields.io/travis/artkonekt/user.svg?style=flat-square)](https://travis-ci.org/artkonekt/user)
[![Packagist Stable Version](https://img.shields.io/packagist/v/konekt/user.svg?style=flat-square&label=stable)](https://packagist.org/packages/konekt/user)
[![StyleCI](https://styleci.io/repos/74651266/shield?branch=master)](https://styleci.io/repos/74651266)
[![Packagist downloads](https://img.shields.io/packagist/dt/konekt/user.svg?style=flat-square)](https://packagist.org/packages/konekt/user)
[![MIT Software License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE.md)

Konekt User is a [Concord module](https://konekt.dev/concord/1.4/modules) that extends
Laravel's built in user/auth functionality with profiles, addresses, organizations.

Internally relies on the [Konekt Address](https://github.com/artkonekt/address) module.

## Important Note On Laravel Auth Support

If the "final" user class is not going to be `App\User` then don't forget to modify model class this to your app's `config/auth.php` file:

```php
    //...
    'providers' => [
        'users' => [
            'driver' => 'eloquent',
            // 'model' => App\User::class <- change this to:
            'model' => Konekt\User\Models\User::class,
        ],
    //...
```

## Laravel Compatibility

| Laravel | Address   |
|:--------|:----------|
| 5.4     | 0.9 - 1.2 |
| 5.5     | 0.9 - 1.4 |
| 5.6     | 0.9 - 1.4 |
| 5.7     | 0.9 - 1.4 |
| 5.8     | 1.0 - 1.4 |
| 6.x     | 1.3+      |
| 7.x     | 1.4+      |
