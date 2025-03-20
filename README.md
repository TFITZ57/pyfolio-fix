# PyFolio Fork with ConfigParser Fix

This is a fork of [pyfolio](https://github.com/quantopian/pyfolio) with a fix for the `SafeConfigParser` issue in newer Python versions.

## The Fix

In newer versions of Python, `SafeConfigParser` was removed and renamed to just `ConfigParser`. This fork makes the following changes:

1. Replaces `configparser.SafeConfigParser()` with `configparser.ConfigParser()`
2. Replaces `parser.readfp()` with `parser.read_file()`
3. Removes the `empyrical` dependency temporarily, as it also has the same issue

## Installation

Install directly from this GitHub repository:

```bash
pip install git+https://github.com/TFITZ57/pyfolio-fix.git
```

## Dependency Note

The original pyfolio depends on `empyrical` which has the same `SafeConfigParser` issue. This fork temporarily removes that dependency to allow installation. For full functionality, you would need to create a similar fix for the empyrical package.

## Original Repository

The original repository can be found at: https://github.com/quantopian/pyfolio 