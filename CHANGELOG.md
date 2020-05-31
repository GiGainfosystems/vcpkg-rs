# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html) as implemented by Cargo.

## [0.2.9] - 2020-05-31

### Added

- add support for `cargo-vcpkg`

## [0.2.8] - 2019-12-01

### Added

- @fungos added the ability to specify the location of a vcpkg tree in code.

## [0.2.7] - 2019-06-29

### Added

- Added support for Linux and MacOS.

### Fixed

- If different versions of a port were installed for different triplets in vcpkg, vcpkg-rs would not be able to find the port in
  some triplets.

## [0.2.6] - 2018-08-21

### Changed

- Extra libraries that are required by optional features will now be linked. For example, if `harfbuzz` is installed with the `icu` feature (making it depend on the `icu` port), libraries from the `icu` port will be linked. Fixes [#7](https://github.com/mcgoo/vcpkg-rs/issues/7)

## [0.2.5] - 2018-08-15

### Changed

- Fix for failure to find packages that have a description that spans multiple lines [#8](https://github.com/mcgoo/vcpkg-rs/issues/8)

## [0.2.4] - 2018-06-14

### Added

- `vcpkg::find_package()` and `vcpkg::Config::find_package()` which follow dependencies and use the correct names for libraries.

### Deprecated

- `vcpkg::probe_package()` and `vcpkg::Config::probe()` are deprecated because they require the filename of the library which can change. Using `vcpkg::find_package()` and `vcpkg::Config::find_package()` will look up the correct names for the DLLs and libraries in the Vcpkg installation.

## [0.2.3] - 2018-04-12

### Changed

- Fix for linking to libraries that contain '.' by @Matrix-Zhang

## [0.2.2] - 2017-06-15

### Added

- This is the initial version
