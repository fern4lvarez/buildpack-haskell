# Buildpack: Haskell

This is a [buildpack](https://www.cloudcontrol.com/dev-center/Platform%20Documentation#buildpacks-and-the-procfile)
for Haskell apps. It uses GHC 7.4.1 and cabal-1.16.0.1.

## Demo

A demo is online here:

http://haskelldemo.cloudcontrolled.com

The demo repo is here:

https://github.com/fern4lvarez/haskell-buildpack-demo

## Usage

    $ ls
    Procfile app.cabal src

    $ cctrlapp APP_NAME create custom --buildpack https://github.com/fern4lvarez/buildpack-haskell.git

    $ cctrlapp APP_NAME/default push
    ...

    -----> Receiving push
    -----> Fetching custom git buildpack... done
    -----> Haskell app detected
    -----> Downloading GHC
    ######################################################################## 100.0%
    -----> Downloading Cabal
    ######################################################################## 100.0%
    -----> Setting up ghc-pkg
    ...

    $ cctrlapp APP_NAME/default deploy
