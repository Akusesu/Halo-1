# Halo 1 Flatpaks

The goal is to make Halo 1 versions available on Linux through wine and flatpaks, enjoy!

# Halo custom edition

Put the files in net.bungie.HCE :
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
flatpak-builder --force-clean builds net.bungie.HCE.yml --install
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
flatpak-builder --force-clean builds net.bungie.HPC.yml --install
```

## Mods

### [Chimera](https://opencarnage.net/index.php?/topic/6916-chimera-build-49/)
What version : Only Halo custom edition

Compatible with : HAC2 and OpenSauce

Installation :
Put the `chimera.dll` in `~/.var/app/net.bungie.Halo1ce/data/wine/dosdevices/c:/Program Files/Microsoft Games/Halo Custom Edition/controls`

### [HAC2](http://blog.haloanticheat.com/)

What version : Custom edition and Retail (PC)

Compatible with : Chimera and OpenSauce (I think it needs something else)

Installation for Halo Custom editon :
Put the `loader.dll` in `~/.var/app/net.bungie.Halo1ce/data/wine/dosdevices/c:/Program Files/Microsoft Games/Halo Custom Edition/controls`

Installation for Halo Retail (PC) :
Put the `loader.dll` in `~/.var/app/net.bungie.Halo1ce/data/wine/dosdevices/c:/Program Files/Microsoft Games/Halo Combat Evolved/controls`
