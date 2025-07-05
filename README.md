# Installation

Gradience can be installed by cloning the PKGBUILD with `git` and building with `makepkg`:

We make sure we have the `base-devel` package group installed.

```bash
sudo pacman -S --needed git base-devel
git clone https://github.com/hydroxycarbamide/Gradience-PKGBUILD.git
cd Gradience-PKGBUILD
makepkg -si
```

Or in a single line:

```bash
sudo pacman -S --needed git base-devel && git clone https://github.com/hydroxycarbamide/Gradience-PKGBUILD.git && cd Gradience-PKGBUILD && makepkg -si
```
