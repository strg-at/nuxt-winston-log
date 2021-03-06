# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

- ...

## [v1.1.0] - 4-13-2020
### Added
- Added reference to winston logger instance from Nuxt `context` object. Access via `context.$winstonLog` from within `asyncData`, `nuxtServerInit`, or other Nuxt lifecyle areas that receive a `context` object.
    - Learn more about the `context` object here: https://nuxtjs.org/api/context
- Added support for passing options to module via inline module options in `nuxt.config.js`
    - For example:
      ```
      ...
      modules: [
        ['nuxt-winston-log', { logName: 'special-logs.log` }]
      ]
      ...
      ```

### Changed
- Updated README w/ information on new `$winstonLog` key in Nuxt `context` objects

## [v1.0.1] - 12-20-2019
### Removed
- Remove stale devDeps

## [v1.0.1] - 12-20-2019
### Changed
- Update README
### Removed
- Cleanup now-defunct `capturePath` option

## [v1.0.0] - 12-20-2019
### Removed
- Remove client side capturing feature. This is best replicated with something like the new [Browser Log Collection features](https://docs.datadoghq.com/logs/log_collection/javascript/?tab=us) in Datadog
### Changed
- Update reqInfo writes to be more succinct
- Improve stack trace passthrough for error captures
- Filter out internal requests to `~/_nuxt/*` assets in access logs
- Filter out non-HTML and non-JSON requests in access logs

## [v0.1.0] - 5-11-2019
### Removed
- Remove `serialize-error` dependency for IE 11 browser compat

## [v0.0.6] - 5-26-2019
### Changed
- Readme fix for new logo path

## [v0.0.3] - 5-26-2019
### Added
- Add a logo, but ignore it from NPM package. No logo for you!

## [v0.0.2] - 5-26-2019
### Added
- Add readme and a changelog
- Add web URLs to `./package.json`

## [v0.0.1] - 5-17-2019
### Added
- Initial bits! 🎉
