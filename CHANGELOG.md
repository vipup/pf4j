## Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

### [Unreleased][unreleased]

#### Fixed

#### Changed

#### Added

#### Removed

### [2.1.0] - 2018-01-10

#### Fixed
- [#177]: Fix Gradle demo
- [#178]: `@Override` should not change method signature
- [#184]: Bug in FileUtils while creating URI on Windows

#### Changed
- [#180]: Refactoring to make `PluginDescriptor` more usable

#### Added

#### Removed

### [2.0.0] - 2017-10-17

#### Fixed
- [#156]: `FileSystemException` when I call `deletePlugin` after `getExtensions`
- Fix Maven warnings

#### Changed
- [#149]: Updated gradle demo dependencies and switched from System.out.println to slf4j log
- Update some code to Java 7
- [#168]: Change root package from `ro.fortsoft.pf4j` to `org.pf4j`
- Open a new extension (protected method) point in `PropertiesPluginDescriptorFinder`

#### Added
- [#146]: Kotlin plugin example added and README updated for Kotlin
- [#150]: Enforce dependencies versions
- [#155]: Add VersionManager abstractization (breaking change)
- [#172]: Add `CompoundPluginDescriptorFinder`
- Add `CompoundPluginLoader`

#### Removed
- Remove `JarPluginManager` (the logic is included in `DefaultPluginManager` via `CompoundXYZ` concept)

### [1.3.0] - 2017-05-03

#### Fixed
- [#129]: Properties Descriptor finder bug fixes and a test
- [#131]: Fix bug in `loadJars()`, did not add `/lib` to classloader
- [#134]: `getVersion()` use wrong class for calculating PF4J version 
- [#135]: `deletePlugin()` failed to delete plugin folder with contents 
- [#137]: The requires Expression does not print well
- [#140]: Unzip plugin zip file in `loadPluginFromPath()`

#### Changed
- [#130]: Refactor validation of PluginDescriptors
- [#138]: Refactor of requires in PluginDescriptor (breaking change) 

#### Added
- [#133]: Support for adding license information to the plugins 
- [#136]: Delete plugin zip on uninstall
- [#139]: Ability to get `pluginsRoot` from PluginManager
- Add constructors with varargs in PippoException

#### Removed

### [1.2.0] - 2017-03-03

#### Fixed
- [#125]: Fix possible NPE

#### Changed
- [#116]: Updated PF4J to newest version in Gradle demo
- Reactivate protection against the issues similar with [#97]

#### Added
- [#128]: Add `JarPluginManager`, `PluginLoader`, `AbstractPluginManager`

#### Removed

### [1.1.1] - 2016-11-17

#### Fixed
- [#116]: Default/System extensions are duplicated

#### Changed

#### Added
- [#111]: Add inheritance support on Extension annotation

#### Removed

### [1.1.0] - 2016-08-22

#### Fixed

#### Changed
- [#107]: PluginDescriptor can't be extended

#### Added
- [#108]: Return a list of all extensions from a plugin and optional for an extension point

#### Removed

### [1.0.0] - 2016-07-07

#### Fixed
- [#99]: NPE in `DefaultPluginManager.stopPlugin()`
- [#100]: Gradle build in demo_gradle is broken
- [#103]: Gradle demos don't build zip with libs
- Fix logging issue in demo

#### Changed
- Rework defense against [#97]
- Eliminate duplicate log messages from demo
- Improve debugging for "no extensions found"

#### Added

#### Removed

### [0.13.1] - 2016-04-01

#### Fixed
- [#98]: WARN ro.fortsoft.pf4j.AbstractExtensionFinder (too many log lines)

### [0.13.0] - 2016-03-28

#### Fixed
- Fix issue with listing files from the jar file in `readPluginsStorages()`
- [#89]: Fix "URI is not hierarchical" issue
- [#91]: Using project lombok with pf4j causes javax.annotation.processing.FilerException

#### Changed
- Log with trace level on PluginClassLoader

#### Added
- Add `distributionManagement` section in `pom.xml`
- Add defense to [#97]
- Add helper `DefaultExtensionFinder.addServiceProviderExtensionFinder()`

#### Removed
- Disable `ServiceProviderExtensionFinder` from `DefaultExtensionFinder`

### [0.12.0] - 2016-01-29

#### Fixed
- [#83]: `stopPlugin()` throws NPE for dependents check
- In development mode hide `plugins/target` folder (it' is not a plugin)

#### Changed
- Add constructor with vararg and make `addFileFilter()` fluent in `AndFileFilter`
- [#84]: remove warn from `DefaultPluginManager.whichPlugin()`
- Pull method `DefaultPluginManager.whichPlugin()` to PluginManager
- Add `getExtensionFactory()` in PluginManager interface

#### Added
- Add constructor with vararg and make addFileFilter method fluent in `AndFileFilter`
- Add `NameFileFilter` and `OrFileFilter`
- [#85]: ExtensionStorage based on Java Service Provider (META-INf/services)

#### Removed

### [0.11.0] - 2015-11-19

#### Fixed
- [#78]: `PluginManager.disablePlugin()` throws UnsupportedOperationExeption

#### Changed
- Make more fields protected in DefaultPluginManager
- [#70]: Improve PluginDescriptorFinder implementations
- Make PluginManager available in Plugin via PluginWrapper

#### Added
- [#66]: Add possibility to overwrite DefaultPluginManager (to create a JarPluginManager)
- Added one more fail test to DefaultPluginFactory
- Added one more fail test to DefaultExtensionFactory
- Added ManifestPluginDescriptorFinder tests

#### Removed

### [0.10.0] - 2015-08-11

#### Fixed
- [#39]: Fix build on JDK 1.8
- [42]: Stop Plugin issue
- [60]: Failed tests

#### Changed
- Improve logging for DefaultExtensionFinder
- Add defense for [#21]: (not find META-INF/extensions.idx)
- [#44]: Replace `Version` class with `semver` lib
- [#55]: Stop plugin leafs first
- [63]: Extended pf4j to allow custom class loaders to be created

#### Added
- [#33]: Add demo build configuration with Gradle
- [#40]: Add Plugin status provider
- [#41]: Added plugin archive source abstraction
- Added test for DefaultPluginRepository

#### Removed

[unreleased]: https://github.com/decebals/pf4j/compare/release-2.1.0...HEAD
[2.1.0]: https://github.com/decebals/pf4j/compare/release-2.0.0...release-2.1.0
[2.0.0]: https://github.com/decebals/pf4j/compare/release-1.3.0...release-2.0.0
[1.3.0]: https://github.com/decebals/pf4j/compare/release-1.2.0...release-1.3.0
[1.2.0]: https://github.com/decebals/pf4j/compare/release-1.1.1...release-1.2.0
[1.1.1]: https://github.com/decebals/pf4j/compare/release-1.1.0...release-1.1.1
[1.1.0]: https://github.com/decebals/pf4j/compare/release-1.0.0...release-1.1.0
[1.0.0]: https://github.com/decebals/pf4j/compare/release-0.13.1...release-1.0.0
[0.13.1]: https://github.com/decebals/pf4j/compare/release-0.13.0...release-0.13.1
[0.13.0]: https://github.com/decebals/pf4j/compare/release-0.12.0...release-0.13.0
[0.12.0]: https://github.com/decebals/pf4j/compare/release-0.11.0...release-0.12.0
[0.11.0]: https://github.com/decebals/pf4j/compare/release-0.10.0...release-0.11.0
[0.10.0]: https://github.com/decebals/pf4j/compare/release-0.9.0...release-0.10.0

[#184]: https://github.com/decebals/pf4j/issues/184
[#180]: https://github.com/decebals/pf4j/pull/180
[#178]: https://github.com/decebals/pf4j/pull/178
[#177]: https://github.com/decebals/pf4j/pull/177
[#172]: https://github.com/decebals/pf4j/pull/172
[#168]: https://github.com/decebals/pf4j/pull/168
[#156]: https://github.com/decebals/pf4j/issues/156
[#155]: https://github.com/decebals/pf4j/pull/155
[#150]: https://github.com/decebals/pf4j/pull/150
[#149]: https://github.com/decebals/pf4j/pull/149
[#146]: https://github.com/decebals/pf4j/pull/146
[#140]: https://github.com/decebals/pf4j/pull/140
[#139]: https://github.com/decebals/pf4j/pull/139
[#138]: https://github.com/decebals/pf4j/pull/138
[#137]: https://github.com/decebals/pf4j/pull/137
[#136]: https://github.com/decebals/pf4j/pull/136
[#135]: https://github.com/decebals/pf4j/pull/135
[#134]: https://github.com/decebals/pf4j/pull/134
[#133]: https://github.com/decebals/pf4j/pull/133
[#131]: https://github.com/decebals/pf4j/pull/131
[#130]: https://github.com/decebals/pf4j/pull/130
[#129]: https://github.com/decebals/pf4j/pull/129
[#128]: https://github.com/decebals/pf4j/pull/128
[#125]: https://github.com/decebals/pf4j/pull/125
[#122]: https://github.com/decebals/pf4j/pull/122
[#116]: https://github.com/decebals/pf4j/issues/116
[#111]: https://github.com/decebals/pf4j/pull/111
[#108]: https://github.com/decebals/pf4j/pull/108
[#107]: https://github.com/decebals/pf4j/issues/107
[#103]: https://github.com/decebals/pf4j/issues/103
[#100]: https://github.com/decebals/pf4j/issues/100
[#99]: https://github.com/decebals/pf4j/issues/99
[#98]: https://github.com/decebals/pf4j/issues/98
[#97]: https://github.com/decebals/pf4j/issues/97
[#91]: https://github.com/decebals/pf4j/issues/91
[#89]: https://github.com/decebals/pf4j/pull/89
[#85]: https://github.com/decebals/pf4j/issues/85
[#84]: https://github.com/decebals/pf4j/issues/84
[#83]: https://github.com/decebals/pf4j/issues/83
[#78]: https://github.com/decebals/pf4j/issues/78
[#70]: https://github.com/decebals/pf4j/issues/70
[#66]: https://github.com/decebals/pf4j/issues/66
[#63]: https://github.com/decebals/pf4j/issues/63
[#60]: https://github.com/decebals/pf4j/issues/60
[#55]: https://github.com/decebals/pf4j/pull/55
[#44]: https://github.com/decebals/pf4j/pull/44
[#42]: https://github.com/decebals/pf4j/pull/42
[#41]: https://github.com/decebals/pf4j/pull/41
[#40]: https://github.com/decebals/pf4j/pull/40
[#39]: https://github.com/decebals/pf4j/pull/39
[#33]: https://github.com/decebals/pf4j/pull/33
[#21]: https://github.com/decebals/pf4j/issues/21
