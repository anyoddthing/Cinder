# Fork Info

This is a fork of cinderlib which adds a MacOS target that builds cinder as a dynaic library to reduce link times when building.

## Usage

- Open the cinder in XCode and build the dyncinder target. This will build an create a hardlink of cinder `/usr/local/lib/libdyncinder.dylib`
- In your mac target of your cinder app
  - Remove cinder from `Other Linker Flags`
  - Add `/usr/local/lib` to `Library Search Path`
  - Drag `/usr/local/lib/libdyncinder.dylib` in the `Linked Frameworks and Libraries` section in the `General` tab

### Cinder 0.9.1dev: [libcinder.org](http://libcinder.org)

<p align="center">
  <img src="https://libcinder.org/docs/_assets/images/cinder_logo.svg" alt="Cinder Logo" width="256" height="auto"/>
</p>

**Cinder is a peer-reviewed, free, open source C++ library for creative coding.**

Please note that Cinder depends on a few submodules. The simplest way to clone it is:<br />
```
git clone --recursive https://github.com/cinder/Cinder.git
```

To get started with Cinder from GitHub, please read this [git setup document](https://libcinder.org/docs/guides/git/index.html). You might also prefer one of our [pre-packaged downloads](https://libcinder.org/download).

Cinder supports OS X, Windows and iOS. It requires Xcode 5.1.1 or later for development on the Mac, and Visual C++ 2013 or later on Windows.

Cinder is released under the [Modified BSD License](docs/COPYING). Please visit [our website](https://libcinder.org) for more information.

Also be sure to check the [User Forum](http://forum.libcinder.org/#AllForums).
