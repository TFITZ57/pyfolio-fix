# PyFolio Fork with ConfigParser Fix

This is a fork of [pyfolio](https://github.com/quantopian/pyfolio) with a fix for the `SafeConfigParser` issue in newer Python versions.

## The Fix

In newer versions of Python, `SafeConfigParser` was removed and renamed to just `ConfigParser`. This fork changes the following line in `versioneer.py`:

```python
# Old line
parser = configparser.SafeConfigParser()

# New line
parser = configparser.ConfigParser()
```

## Installation

Install directly from this GitHub repository:

```bash
pip install git+https://github.com/yourusername/pyfolio-fix.git
```

Replace `yourusername` with your actual GitHub username after you fork and push this repository.

## Original Repository

The original repository can be found at: https://github.com/quantopian/pyfolio 