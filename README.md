# Introduction

This project is a POC to sync up a local access (windows) collection of tables to mysql DB on a secured remote server (through SSH)

The program is built from golang in linux (cross compiling)

# Getting started

From a linux box:

## Requirements

- docker 1.8 or higher

## Steps

- Initialize your build environment:

    ```bash
    mkdir ~/src/go/src
    cd ~/src/go/src
    git clone https://github.com/clarsonneur/matos_sync
    # If you are running docker without sudo
    source build-env.sh ~/src/go
    # If you are running docker with sudo
    source build-env.sh --sudo ~/src/go
    build.sh
    ```

## Windows machine requirements

On the windows machine, you need to install the appropriate `AccessDatabaseEngine` package aligned with your MS Access installation.

The binary is a 32 bits, so, you need to install the 32bits library as well.

For MS Access 2007, I installed the following:
https://www.microsoft.com/en-us/download/confirmation.aspx?id=13255

# TODO

- Expose Matos DB as a REST API to just read it.
- Expose Matos DB as a REST API to update it if needed.