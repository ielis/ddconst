# How to release

## How to release into *PyPi* repository:
1. do all the usual Git stuff
2. build Python binaries, use the interpreter/virtual environment where all the required libraries are installed:
    ```bash
    python setup.py sdist bdist_wheel bdist_egg
    ```
    > the command above will populate the `dist/` directory with package binaries
3. upload binaries to *PyPi*, use the interpreter where the package `twine` is installed
    ```bash
    python -m twine upload -s -i <key_id> dist/*
    ```
    > - `-s` - require signing of packages
    > - `-i` - identity of the PGP key to use for signing
    
*Done!*

## How to install into a local virtual environment:

1. do all the usual Git stuff
2. run 
    ```bash
    cd ddconst
    pip install -e ./
    ```
   > This installs the development version of the package, where changes are automatically available within the environment
