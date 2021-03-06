
  [@dwijnand]: http://github.com/dwijnand
  [1828]: https://github.com/sbt/sbt/issues/1828
  [1992]: https://github.com/sbt/sbt/pull/1992

### Fixes with compatibility implications

- Starting 0.13.9, `crossScalaVersions` default value is fixed back to the older 0.12.x behavior. See below for
  details

### Improvements

### Bug fixes

### `crossScalaVersions` default value

As of this fix `crossScalaVersions` returns to the behaviour present in `0.12.4` whereby it defaults to what
`scalaVersion` is set to, for example if `scalaVersion` is set to `"2.11.6"`, `crossScalaVersions` now defaults
to `Seq("2.11.6")`.

Therefore when upgrading from any version between `0.13.0` and `0.13.8` be aware of this new default if
your build setup depended on it.

[#1828][1828]/[#1992][1992] by [@dwijnand][@dwijnand]
