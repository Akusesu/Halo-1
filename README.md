# Halo 1 Flatpaks

The goal is to make Halo 1 versions available on Linux through wine and flatpaks, enjoy!

# Halo custom edition

Put the files in net.bungie.Halo1ce :
- halocesetup_en_1.00.exe
- haloce-patch-1.0.10.exe

Install required Winepak packages :
```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak remote-add --if-not-exists winepak https://dl.winepak.org/repo/winepak.flatpakrepo
flatpak install winepak org.winepak.Platform//3.0
flatpak install winepak org.winepak.Sdk//3.0
```
Then build and install it
```
flatpak-builder --force-clean --repo test builds net.bungie.Halo1ce.yml --install
```

# Halo combat evolved

Put the files in net.bungie.Halo1pc :

- halo-setup
  - Setup.Exe
  - ...
- halopc-patch-1.0.10.exe

Install required Winepak packages :
```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak remote-add --if-not-exists winepak https://dl.winepak.org/repo/winepak.flatpakrepo
flatpak install winepak org.winepak.Platform//3.0
flatpak install winepak org.winepak.Sdk//3.0
```
Then build and install it
```
flatpak-builder --force-clean --repo test builds net.bungie.Halo1pc.yml --install
```

## Mods

### [Chimera](https://opencarnage.net/index.php?/topic/6916-chimera-build-49/)
What version : Only Halo custom edition

Compatible with : HAC2 and OpenSauce

Installation :
Put the `chimera.dll` in `~/.var/app/net.bungie.Halo1ce/data/wine/dosdevices/c:/Program Files/Microsoft Games/Halo Custom Edition/controls`
