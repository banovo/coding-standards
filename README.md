# Banovo Coding Standards

[![Build Status](https://travis-ci.org/banovo/coding-standards.svg?branch=master)](https://travis-ci.org/banovo/coding-standards)

## Installation

Add to `composer.json`:

```json
"require-dev": {
    "banovo/coding-standard": "0.1.*"
}
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

Execute `bin/checker` locally to see errors

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
