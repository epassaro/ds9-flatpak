# ds9-flatpak
Flatpak build recipe for SAOImage DS9

## Installation

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
$ flatpak run com.github.SAOImageDS9.SAOImageDS9.yml
```
