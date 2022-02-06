---
layout: layout.njk
title: install
---

## Installation

`swhkd` and `swhks` install to `/usr/local/bin/` by default. You can change this behaviour by editing the Makefile variable, `TARGET_DIR`.

# Dependencies:

## Runtime:

-   Policy Kit Daemon ( polkit )

## Compile time:

-   `rustup`
-   `make`

# Compiling:

-   `git clone https://github.com/waycrate/swhkd`
-   `make setup`
-   `make clean`
    -   `make` for a musl compile.
    -   `make glibc` for a glibc compile.
-   `sudo make install`

# Running:

`pkexec swhkd`
