# How to release

## How to release into *PyPi* repository:
1. do all the usual Git stuff

2. build Python binaries, use the interpreter/virtual environment where all the required libraries are installed:
    ```bash
    python3 build
    ```
    > The command builds the source code and stores the artifacts in the `dist/` directory

3. upload binaries to *PyPi*, use the interpreter where the package `twine` is installed
    ```bash
    python -m twine upload dist/*
    ```

## How to install into a local virtual environment:

1. do all the usual Git stuff
2. run 
    ```bash
    cd ddconst
    python3 -m pip install -e .
    ```
   > This installs the development version of the package, where changes are automatically available within the environment
