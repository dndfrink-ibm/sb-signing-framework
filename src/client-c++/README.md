# Dependencies

- meson/ninja (not needed if building with make)
- cmake (not needed if building with make)
- g++/clang++
- json-c
- openssl
- curl-devel

# Linux Build Notes

## Compile

Only building sf_client:
```
meson build -Dlib-pkcs11=false
ninja -C build
```

Building sf_client and the pkcs11 shared library module:
```
meson build -Dlib-pkcs11=true
ninja -C build
```

## Install

```
meson install
```

# AIX Build Notes

A Makefile has been provided as an easier sf_client build solution for AIX.

This Makefile is compatible with GNU make, which can be installed from the AIX toolbox.

GNU make is provided via the `make` package and is installed by default to `/opt/freeware/bin/make`.

## Compile

```
/opt/bin/freeware/make
```
