![](assets/apio-banner.svg)

# Apio Developers Environment

## Forking the Apio repository
The first step in developing for Apio is to fork the Apio repository. This will allow you to run run all the test workflow before submitting your pull request.  In the rest of this document we assume that foked the Apio repository and cloned it locally on your computer.

## Installing your cloned repo using Pip

Having the Pip `apio` package installed from your local cloned repo will allow you to run `apio` commands locally using your latest code. This step greatly simplified the edit/test/repeat development cycle and is highly recomanded.

Run this in the repo's root directory where the file `pyproject.toml` resides.
```
# In case apio is installed
pip uninstall apio

# Install the repo as the the Pip `apio` package.
pip install -e .

# Confirming Apio 'Apio Python package' dir.
apio info system
```

## Test your changes before committing to your forked repo.
Before committing your changes to your forked Apio repository run the following command in the repo root directory.  This will run the linters and then use pytest to run all the offline and online tests and can take a few minutes to complete

```shell
make check
```

During debugging its sometime useful to run partial and quick tests that that covered the area being worked on. Below are some examples for partial test you can run (always in the root directory of your repo)   

```shell
# Run linters only
make lint

# Offline tests only. These are test that don't fetch remote Apio packages.
make test

# Run a single test file with verbose info
pytest -vv -s test/managers/test_project.py

# Run a single test with verbose info
pytest -vv -s test/managers/test_project.py::test_first_env_is_default
```

> The page `htmlcov/index.html` shows the coverage of the last test run. The directory `htmlcov` is transient and is ignored by git.

## Confirm that the test workflows passed before sending a pull request.

Each time you commit to your forked apio repo, github runs the apio test workflows with various combination of OS, OS versions, and Python versions. Before sending a pull request to the Apio team, make sure that all the test of your last commit passed. You can find the test results in the `actions` tab of your github repo dashboard.

## Using APIO_DEBUG to print debug information

If the env var `APIO_DEBUG` is defined (regardless of its value), Apio emits internal debugging information that may be useful for debugging.

```
# Linux and Mac OSX
export APIO_DEBUG=

# Windows
set APIO_DEBUG=
```




## Running apio in the Visual Studio Code debugger.

The `.vscode/launch.json` file contains debugging targets for the Visual Studio Code (VSC) debugger. To use them, make sure that you open the Apio project at its root directory and select the desired VCS debugging target. To customize the targets for your specific need, click on the Settings icon (wheel) near the debugging target and edit it's definition in `launch.json` (do not submit changes to `launch.json` unless they will benefit other developers).

Since Apio launches Scons as a subprocess, **debugging the Scons code require a different approach** using these steps:

1. Set the env var `APIO_SCONS_DEBUGGER` to cause scons waiting for the debugger (in `apio/scons/SConstruct`)
2. Set your desired breakpoints in the scons part of apio.
3. From the command line, run the apio command that invokes the scons subprocess (e.g. `apio build`)
4. In the VSC debugger, start the target `Attach remote debugger`

<br>

![](assets/fpgawars-banner.svg)