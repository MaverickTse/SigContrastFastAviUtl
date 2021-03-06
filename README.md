# Sig(De)ContrastFastAviUtl

Sigmoidal contrast and decontrast Aviutl plugin. ImageMagick is not being used.

# Build Tips

Should be easy to build as there are no external dependency (except for VS2015 redist). There is a property sheet in the project that set a macro for AviUtl's path. By default, DEBUG auf will be in the same folder as aviutl.exe, while RELEASE build will be put inside the \plugins folder.

# Known issues

* parameter change may not reflect properly if you change the parameters while the plugin is disabled.
* It sucks: fork your own

# Technical details

* Dumpped IM library -> reduce memory footprint and overhead
* using ``std::thread`` for  parallelization/vectorization
* Use table lookup to reduce calculation
* Two plugins in a single AUF

# Dependency

## for AviUtl plugin

**Nothing**. ImageMagick or OpenCV is not used.

## for test

- [iutest](https://github.com/srz-zumix/iutest) - c++ testing framework

Use

```sh
git clone --recursive https://github.com/MaverickTse/SigContrastFastAviUtl.git
```

or 

```sh
git clone https://github.com/MaverickTse/SigContrastFastAviUtl.git
git submodule update --init
```

to download dependency.
