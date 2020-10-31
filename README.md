CalcHEP flatpak
===============

This repository provides a distribution agnostic way to install
[CalcHEP](https://theory.sinp.msu.ru/~pukhov/calchep.html) via Flatpak

Installation
------------
- Make sure that flatpak and flatpak-builder are installed
- Install the software development kit
```
flatpak install flathub org.freedesktop.Platform//20.08 org.freedesktop.Sdk//20.08
```
- Compile and install CalcHEP locally
```
flatpak-builder build-dir ru.msu.sinp.theory.CalcHEP.yaml --force-clean --install --user
```

Usage
-----
The CalcHEP tools are available via
```
flatpak run ru.msu.sinp.theory.CalcHEP <command>
```
For example
```
flatpak run ru.msu.sinp.theory.CalcHEP mkWORKdir my-fancy-new-workdir
flatpak run ru.msu.sinp.theory.CalcHEP set_param ...further...arguments...
flatpak run ru.msu.sinp.theory.CalcHEP ./calchep
```
If `<command>` is ommitted, a list of available commands is shown.
