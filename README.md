# Example documentation

This is an example of how to structure a set of [Markdown](https://daringfireball.net/projects/markdown/) documentation, for building with the [documentation builder](https://docs.ubuntu.com/documentation-builder/en/).

## Usage

To build documentation, you first need to install the documentation-builder:

``` bash
snap install documentation-builder
```

Then, navigate to the folder containing this repository and run the command

``` bash
documentation-builder
```

This will build HTML documentation in the `build/` directory. You can now view it in a browser by opening `build/en/index.html`.

