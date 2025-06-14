![](assets/apio-banner.svg)

# Installing Apio as a Python Pip package

Apio can be installed as a Pip package that relies on a Python installation, or standalone, using packages, installers, and file bundles that contains all the files that are required. This page describe the Python based Pip package installation.

<br>

**Install**

1. Run `python --version` and verify that it matches the [Apio system requirements](system-requirements).

2. Install the latest Apio code by running the following command.

```
pip install --force-reinstall -U git+https://github.com/FPGAwars/apio.git@develop#egg=apio
```

3. Open a new shell window and type `apio system info` to test your installation.

<br>

**Uninstall**

1. Delete the `apio` pip package by running `pip uninstall apio`.

2. Delete the Apio settings directory `.apio` under your home directory.

<br>

![](assets/fpgawars-banner.svg)