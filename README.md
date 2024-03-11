# Playground Documentation

This repository provides the documentation for the Playground Application
Ecosystem.

## Installation

Building documentation uses [Python 3](https://www.python.org/).

Install [Sphinx](http://www.sphinx-doc.org/) for building documentation.

```sh
pip install sphinx
```

Install the [Sphinx theme](https://github.com/readthedocs/sphinx_rtd_theme)
```sh
pip install sphinx-rtd-theme
```

Further reading:
- [Read the Docs: Getting started with Sphinx](https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html)

## Build

- See Makefile: https://github.com/readthedocs/readthedocs-build/blob/master/docs/Makefile

```sh
make clean
```
- Clean up before building

### Document formats

```sh
make html
```

```sh
make json
```

```sh
make text
```

```sh
make man
```

### Document tools

```sh
make changes
```

```sh
make linkcheck
```

```sh
make help
```