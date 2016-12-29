# Awesome CET library
Awesome aims to deliver a set of tools that facilitates your life when writing code for [Configura] (http://www.configura.com/) plaftorm.

## Usage
- Download and install [Visual Studio Code](https://code.visualstudio.com/download)
- Make sure you have the latest suported version of [vscode-cm](https://github.com/felipegtx/vscode-cm/releases) plugin installed
- Download the latest version of `Awesome` and add it to your project

### gitignore
We recomend adding `.cmx` extension to your project's gitignore file.

## MPC
Awesome was created 

## Awesome Components
Awesome ships with a bunch of core components that when used togheter enables you to build a simple yet complete solution.

The main components in the library are the following:

### AweGeometry
Provides access to the visual representation of your products. 

### AweProduct
A logic representation of a given product with all its features.

### AweMPC`<Model, Product>` 
Bundles the core functionalities for your *Controller*.

## Remarks

### `X` redefines (SMemberSyntax)
If you are getting this error you have `Awesome` inside the `custom` plugins in your CET. Remove it, run a `Clean CMX` in your project and try again.
