# Banovo Coding Standards

[![Build Status](https://travis-ci.org/banovo/coding-standards.svg?branch=master)](https://travis-ci.org/banovo/coding-standards)

## Installation

Add to `composer.json`:

```json
"require-dev": {
    "banovo/coding-standard": "0.3.*"
},
"scripts": {
    "post-install-cmd": [
        "echo 'bin/checker' > .git/hooks/pre-commit"
    ],
    "post-update-cmd": [
        "echo 'bin/checker' > .git/hooks/pre-commit"
    ]
},

```

Add pre-commit hook
```
echo './vendor/bin/php-cs-fixer fix --config=./vendor/banovo/coding-standard/rulesets/.php_cs.dist src && git add .' > .git/hooks/pre-commit
```

## Usage

Pre-commit hook will execute checker automatically,
when you run `git commit`.

Execute `bin/checker -h` to see additional configuration.

## Update

Ensure it is up-to-date:

* `rulesets/Symfony` folder is a copy from [Symfony Coding Standard](https://github.com/djoos/Symfony-coding-standard)
 
* `rulesets/SlevomatCodingStandard` folder is a copy from [Slevomat Coding Standard](https://github.com/slevomat/coding-standard)
