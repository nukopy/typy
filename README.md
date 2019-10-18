# Typy: simple wrapper of Mypy

"Typy" is very simple wrapper of "[Mypy](https://github.com/python/mypy)", which is an optional static type checker for Python.

## Requirements

You need Python 3.5 or later to run typy(mypy require this).

### Mypy install

In MacOS, Mypy can be installed using pip:

```bash
$ pip install mypy
```

For other environments, packages are available at [http://www.python.org/getit/](http://www.python.org/getit/).

## Quick start

### Typy install

- git clone

**Recommendation: you should install typy to a directry your original alias files is in.**

```bash
$ git clone git@github.com:python/typy.git
```

### Set up command alies

- Give excecute permission to `typy`

```code
$ cd typy
$ chmod u+x typy
```

- Set up command alias

Add following line to `~/.bashrc` or `~/.bash_profile`:

```bash
alias typy="full/path/to/typy"
```

Reloading shell, you can use typy.

## Quick Test

This repository contains quick test for typy.

### Pass type checking

```bash
$ cd typy
$ typy test_success.py
```

output

```txt
------------ type checking -------------
Success: no issues found in 2 source files

 -------------- run script --------------
Pass Type Checking!!
```

### Fail type checking

```bash
$ typy test_failed.py
```

output

```txt
------------ type checking -------------
test_failed.py:2: error: Incompatible return value type (got "int", expected "str")
Found 1 error in 1 file (checked 2 source files)
```
