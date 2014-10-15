# Haskell

![Haskell logo](../master/img/haskell_logo.png?raw=true)

# Basic info about the image

Tags: `latest`

ghc version : 7.8.3

cabal-install version: 1.20.0.3, using version 1.20.0.0 of the Cabal library

## What is Haskell?

Haskell is an advanced purely-functional programming language. An open-source product of more than twenty years of cutting-edge research,
it allows rapid development of robust, concise, correct software. With strong support for integration with other languages, built-in concurrency and parallelism,
debuggers, profilers, rich libraries and an active community, Haskell makes it easier to produce flexible, maintainable, high-quality software.

## How to use

### First pull the image locally

    docker pull denibertovic/haskell


### Run an interactive bash prompt

    # this will run a bash prompt in the container
    # where you can use cabal, ghci and so on
    docker run -i -t denibertovic/haskell

### Mount your code directory in the container

    # this allows you to compile the code in the container
    # while still working on it on the host in your favorite editor
    docker run -v /path/to/code/on/host:/code -i -t denibertovic/haskell

### Compile code

    docker run -v /path/to/code/on/host:/code -i -t denibertovic/haskell ghc /code/Main.hs

### You can use cabal inside the container

    docker run -v /path/to/code/on/host:/code -i -t denibertovic/haskell
    root@b7f76916678b:/code# cabal update
    root@b7f76916678b:/code# cabal sandbox init
    root@b7f76916678b:/code# cabal build

