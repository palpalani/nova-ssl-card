# Nova SSL Card

[![Latest Version on Packagist](https://img.shields.io/packagist/v/marianvlad/nova-ssl-card.svg?style=flat-square)](https://packagist.org/packages/marianvlad/nova-ssl-card)
[![Total Downloads](https://img.shields.io/packagist/dt/marianvlad/nova-ssl-card.svg?style=flat-square)](https://packagist.org/packages/marianvlad/nova-ssl-card)
[![GitHub Tests Action Status](https://img.shields.io/github/workflow/status/marianvlad/nova-ssl-card/run-tests?label=tests)](https://github.com/palpalani/nova-ssl-card/actions?query=workflow%3Arun-tests+branch%3Amain)
[![GitHub Code Style Action Status](https://img.shields.io/github/workflow/status/marianvlad/nova-ssl-card/Check%20&%20fix%20styling?label=code%20style)](https://github.com/palpalani/nova-ssl-card/actions?query=workflow%3A"Check+%26+fix+styling"+branch%3Amain)

Get details about SSL certificate inside a Nova card.

![nova-ssl-card](https://i.imgur.com/KOCjCj3.png)

## Installation

You can install the package in to a Laravel app that uses [Nova](https://nova.laravel.com) via composer:

```bash
composer require marianvlad/nova-ssl-card
```

Next up, you must register the card Nova. This is typically done in the `cards` method of the `NovaServiceProvider`.

```php
// in app/Providers/NovaServiceProvider.php

// ...

public function cards()
{
    return [
        // ...
        new \Marianvlad\NovaSslCard\NovaSslCard,
    ];
}
```
 
## Usage

By default, the card will show certificate details for the current domain
where you have installed Nova, but you can configure for any domain name

```php
// in app/Providers/NovaServiceProvider.php

// ...

public function cards()
{
    return [
        new \Marianvlad\NovaSslCard\NovaSslCard, // current domain
        // or
        new \Marianvlad\NovaSslCard\NovaSslCard('laravel.com'),
    ];
}
```

## Testing

```bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](.github/CONTRIBUTING.md) for details.

## Security Vulnerabilities

Please review [our security policy](../../security/policy) on how to report security vulnerabilities.

## Credits

- [palPalani](https://github.com/palpalani)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
