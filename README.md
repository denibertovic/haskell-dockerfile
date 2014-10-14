# Haskell runtime

ghc version : 7.8.3

cabal-install version: 1.20.0.3, using version 1.20.0.0 of the Cabal library

## How to use

    docker pull denibertovic/haskell
    # this will run a bash prompt in the container
    # where you can use cabal, ghci and so on
    docker run -i -t denibertovic/haskell

    # You can also mount your code directory in the container
    docker run -v /path/to/code/on/host:/code -i -t denibertovic/haskell

