# Banovo Coding Standards
A coding standard to check against the Banovo php coding standards, originally shamelessly copied from the [djoos/Symfony-coding-standard](https://github.com/djoos/Symfony-coding-standard) repository.

## Installation

### Composer

This standard can be installed with the [Composer](https://getcomposer.org/) dependency manager.

#### 1. [Install Composer](https://getcomposer.org/doc/00-intro.md)

#### 2. Install the coding standard as a dependency of your project

```bash
composer require --dev escapestudios/symfony2-coding-standard:3.x-dev
```

#### 3. Add the coding standard to the PHP_CodeSniffer install path

```bash
vendor/bin/phpcs --config-set installed_paths vendor/escapestudios/symfony2-coding-standard
```

#### 4. Check the installed coding standards for "Symfony"

        vendor/bin/phpcs -i

#### 5. Done!

        vendor/bin/phpcs /path/to/code

### Stand-alone

#### 1. Install [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)

#### 2. Checkout this repository 

```bash
git clone git://github.com/djoos/Symfony2-coding-standard.git
```

#### 3. Add the coding standard to the PHP_CodeSniffer install path

```php
phpcs --config-set installed_paths /path/to/Symfony2-coding-standard
```

Or copy/symlink this repository's "Symfony"-folder inside the phpcs `Standards` directory

#### 4. Check the installed coding standards for "Symfony"

```bash
phpcs -i
```

#### 5. Done!

```bash
phpcs /path/to/code
```
