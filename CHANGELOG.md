# Change Log

All notable changes to this project will be documented in this file
and is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

This project follows the version scheme MAJOR.MINOR.COMMITS where
MAJOR and MINOR provide some relative indication of the size of the
change, but do not follow semantic versioning. In general, all changes
endeavour to be non-breaking (by moving to new names rather than by
breaking existing names). COMMITS is an ever-increasing counter of
commits since the beginning of this repository.

## [Unreleased]

### Changed
### Added
### Removed

## [5.0.152]

- Update Sentry Java SDK to 5.1.2

## [5.0.151]

- Update Sentry Java SDK to 5.1.1
- Minor updates

## [5.0.149]

- Updated Sentry Java SDK to 5.0.1

## [5.0.147]

- Updated Sentry Java SDK to 5.0.0
- No other functional changes

## [4.3.146]

- Fix request method as string. Thanks to @danieltdt!

## [4.3.143]

### Fixed

- Allow simple strings (as well as maps) to be used for the message.
  Thanks to @bago2k4 for the contribution! :-) Fixes #23
- Bump Sentry to 4.3.0

## [4.2.139]

### Changed

- Changed CLOJARS_REPO to CLOJARS_URL in the deployment script
- Formatting changes to various documents
- Bump Sentry to 4.2.0

## [3.1.138]

### Added

- Added [Contexts](https://docs.sentry.io/platforms/java/enriching-events/context/)
  to the initialisation of Sentry so that additional information can
  be sent upon each event. Further information contained within the
  README.md and in `sentry_clj/core.clj`. **Note:** `:extras` has been
  deprecated by Sentry - use `:contexts` instead.

## [3.1.137]

### Changed

- Bump Sentry to 3.2.1
- Bump up ring-core to 1.8.2

## [3.1.135]

### Added

- Added in `before-send-fn` and `before-breadcrumb-fn` to the
  initialisation map. This allows for events or breadcrumbs to be
  mutated before sending off to Sentry (or indeed to *prevent* sending
  to Sentry if the respective functions returns nil)

## [3.1.134]

### Changed

- Don't default the environment to "production" if none if found on
  the event, let the Java library do that now.
- Bumped Sentry Java 3.2.0.

## [3.1.130]

### Added

- Added in missing clj-kondo config.

### Changed

- Fix ring handler to work with new Sentry data structure.
- Bumped `deps-deploy`.
- Remove unused 'mocko' library.
- Set warn-on-reflection to be true.

## [3.1.127]

### Added

- Added in a simple deploy script.

### Changed

- Moved to the major.minor.commit model.
- Removed unused library `clojure.java-time`.
- Updated pom.xml with some additional metadata information.
- Bumped Sentry Java to 3.1.1.

## [3.1.0]

### Added

- Added in the ability to define the Environment on configuration of
  Sentry (and not only per-event!)
- Added in the ability to disable the built-in
  UncaughtExceptionHandler in order to allow defining our own.
- Added in a couple of examples:
  - A basic example showing how to register a sentry-logger and how to
    fire an event.
  - An example that registers it's own uncaught exception handler to
    not only log out to sentry, but also to log out to a
    pre-configured logger.

### Changed

- Major release bringing compatibility with version 3.1.0 of the Java
  Sentry library. This is a **BREAKING** change, insofar that this has
  only been tested with the latest Sentry (20.9.0) and is **not**
  compatible with Sentry 10.0.1 and below. If you wish to use those
  versions, please continue to use sentry-clj 1.7.30.

[Unreleased]: https://github.com/getsentry/sentry-clj/compare/5.0.152...HEAD
[5.0.152]: https://github.com/getsentry/sentry-clj/compare/5.0.151...5.0.152
[5.0.151]: https://github.com/getsentry/sentry-clj/compare/5.0.147...5.0.151
[5.0.149]: https://github.com/getsentry/sentry-clj/compare/5.0.147...5.0.149
[5.0.147]: https://github.com/getsentry/sentry-clj/compare/4.3.146...5.0.147
[4.3.146]: https://github.com/getsentry/sentry-clj/compare/4.3.143...4.3.146
[4.3.143]: https://github.com/getsentry/sentry-clj/compare/4.2.139...4.3.143
[4.2.139]: https://github.com/getsentry/sentry-clj/compare/3.1.138...4.2.139
[3.1.138]: https://github.com/getsentry/sentry-clj/compare/3.1.137...3.1.138
[3.1.137]: https://github.com/getsentry/sentry-clj/compare/3.1.135...3.1.137
[3.1.135]: https://github.com/getsentry/sentry-clj/compare/3.1.134...3.1.135
[3.1.134]: https://github.com/getsentry/sentry-clj/compare/3.1.127...3.1.134
[3.1.0]: https://github.com/getsentry/sentry-clj/compare/3.1.0...3.1.127
