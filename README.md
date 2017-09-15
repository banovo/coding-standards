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

Add to `wercker.yml`:

```yml
build:
    steps:
        - script:
            name: Coding Standards and Syntax Check
            code: bin/checker
```

## Usage

Pre-commit hook will execute checker automatically,
when you run `git commit`.

Execute `bin/checker` manually if you want to change default configuration:

```
# Usage:
#   bin/checker [branch] [type] [fix]
#
#   branch:
#     > master   - use branch origin/master as base for diff
#       <branch> - use branch origin/<branch> as base for diff
#
#   type:
#       all     - all files in repository
#     > diff    - diff of all changed files (staged and unstaged)
#       staged  - diff of only staged files
#
#   fix:
#     > nofix   - no fix
#       fix     - run fix
```

## Update

`rulesets/Symfony` folder is a copy from [Symfony-coding-standard repository](https://github.com/djoos/Symfony-coding-standard).
 Ensure it is up-to-date.
