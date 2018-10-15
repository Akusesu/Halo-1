# Halo 1 Flatpaks

The goal is to make Halo 1 versions available on Linux through wine and flatpaks, enjoy!

# Halo custom edition

Put the files in the build directory :
- halocesetup_en_1.00.exe
- haloce-patch-1.0.10.exe

Then build and install it
```
flatpak-builder --force-clean --repo test builds net.bungie.Halo1ce.yml --install
```
