# ds9-flatpak
Flatpak build recipe for SAOImage DS9

## Installation

Requires `flatpak` and `flatpak-builder` installed on your system.

```bash
# Clone the repository
$ git clone https://github.com/epassaro/ds9-flatpak.git && cd ds9-flatpak

# Install flatpak-builder
$ sudo apt install flatpak-builder

# Add the Flathub repository
$ flatpak remote-add --user --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo

# Install the runtime and SDK
$ flatpak install --user flathub org.freedesktop.Platform//22.08 org.freedesktop.Sdk//22.08

# Build the package
$ flatpak-builder --force-clean build_dir com.github.SAOImageDS9.SAOImageDS9.yml

# Install the package
$ flatpak-builder --user --install --force-clean build_dir com.github.SAOImageDS9.SAOImageDS9.yml

# Run the package
$ flatpak run com.github.SAOImageDS9.SAOImageDS9
```

## Motivation
I began this project primarily for research purposes because I've been wanting to learn how to distribute software in the Flatpak format for a while. 

I decided to start with DS9 because it's a piece of software I'm familiar with, and it's relatively easy to build.

## See also
- [PackagingLab](https://epassaro.github.io/packaginglab) - Project website 
- [ds9-appimage](https://github.com/epassaro/ds9-appimage) - My DS9 builds in the AppImage format
- [ds9-feedstock](https://github.com/conda-forge/ds9-feedstock) - My conda-forge recipe for DS9
