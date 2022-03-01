---
layout: layout.njk
title: Install
---
# AUR:
`swhkd-git` `swhkd-musl-git` have been packaged. `swhkd-bin` & `swhkd-musl-bin` will be released soon.

## Installation

`swhkd` and `swhks` install to `/usr/local/bin/` by default. You can change this behaviour by editing the Makefile variable, `TARGET_DIR`.

# Dependencies:

## Runtime:

-   Policy Kit Daemon ( polkit )

## Compile time:

-   rustup
-   make

# Compiling:

-   `git clone https://github.com/waycrate/swhkd && cd swhkd`
-   `make setup`
-   `make clean`
    -   `make` for a musl compile.
    -   `make glibc` for a glibc compile.
-   `sudo make install`

# Running:
`swhks`
`pkexec swhkd`
