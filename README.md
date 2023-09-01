# ds9-flatpak
Flatpak build recipe for SAOImage DS9

## Installation

```
$ git clone https://github.com/epassaro/ds9-flatpak.git && cd ds9-flatpak
$ flatpak-builder --user --install --force-clean build-dir com.github.SAOImageDS9.SAOImageDS9.yml
$ flatpak run com.github.SAOImageDS9.SAOImageDS9.yml
```
