---
layout: layout.njk
title: Wayshot
---

<p align=center>
  <img src="{{ '/assets/img/wayshot.png' | url }}" alt=wayshot width=60%>
  <p align=center>A native screenshot tool for Wayland (X11 support coming soon) written in Rust. <a href="https://github.com/waycrate/wayshot">GitHub</a></p>
  
  <p align="center">
  <img src="https://img.shields.io/github/license/waycrate/wayshot?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/badge/cargo-v1.0.0-green?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/issues/waycrate/wayshot?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/forks/waycrate/wayshot?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/stars/waycrate/wayshot?style=flat-square&logo=appveyor">
  </p>
</p>

# Usage:

**Note: The project is a WIP.**

Region Selection:

```bash
wayshot -s "$(slurp -f '%x %y %w %h')" > /tmp/image.png
```

Fullscreen:

```bash
wayshot > /tmp/image.png
```

Screenshot and copy to clipboard:

```bash
wayshot | wl-copy
```

Pick a hex color code, using ImageMagick:

```bash
wayshot -s "$(slurp -p -f '%x %y %w %h')" | convert - -format '%[pixel:p{0,0}]' txt:-|egrep "#([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})" -o
```

Pick a color, using ImageMagick:

```bash
wayshot -s "$(slurp -p -f '%x %y %w %h')" | convert - -format '%[pixel:p{0,0}]' txt:-
```

# Installation
## AUR:
`wayshot-git`has been packaged. `wayshot-bin` will be released soon.

## Compile time dependencies:
-   rustup
-   make

## Compiling:
-   `git clone https://github.com/waycrate/wayshot && cd wayshot`
-   `make setup`
-   `make clean`
    -   `make`
    -   `make glibc`
-   `sudo make install`

# Support server:

[Discord](https://discord.gg/KKZRDYrRYW)

# Contributors:

<a href="https://github.com/waycrate/wayshot/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=waycrate/wayshot" />
</a>

# Cmeissl: 

Massive thanks to Smithay contributor [Cmeissl]("https://github.com/cmeissl"). Without them this project won't be possible as my wayland knowledge is very very limited.
