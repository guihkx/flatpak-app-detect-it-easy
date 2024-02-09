# About

Detect It Easy is an advanced file analyzer.

More information at: https://github.com/horsicq/Detect-It-Easy

# Installation

First, download the latest version from the [Releases page](https://github.com/guihkx/flatpak-app-detect-it-easy/releases).

To install the package for all users, open a terminal window and run:

```bash
flatpak install detect_it_easy*-x86_64.flatpak
```

And you're good to go. You should find Detect It Easy in your apps list.

# Advanced

## Building

Before proceding, make sure both `flatpak` and `flatpak-builder` packages are installed.

64-bit AMD/Intel:

```bash
# Build
flatpak-builder --arch x86_64 --delete-build-dirs --force-clean --install-deps-from flathub --repo repo/ --sandbox builddir/ io.github.horsicq.detect_it_easy.yaml
# Create a single-bundle file
flatpak build-bundle --arch x86_64 repo/ detect_it_easy-x86_64.flatpak io.github.horsicq.detect_it_easy master
# Install it
flatpak install --bundle detect_it_easy-x86_64.flatpak
```

64-bit ARM:

```bash
# Build
flatpak-builder --arch aarch64 --delete-build-dirs --force-clean --install-deps-from flathub --repo repo/ --sandbox builddir/ io.github.horsicq.detect_it_easy.yaml
# Create a single-bundle file
flatpak build-bundle --arch aarch64 repo/ detect_it_easy-x86_64.flatpak io.github.horsicq.detect_it_easy master
# Install it
flatpak install --bundle detect_it_easy-aarch64.flatpak
```
