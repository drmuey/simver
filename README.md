# simver

Simple Versioning Specification (SimVer) 1.0

# Spec

1. Keep a proper changelog (e.g. the “[Keep a Changelog](http://keepachangelog.com/en/1.0.0/)” format).
2. Given a version number MAJOR.MINOR, _on release_, increment the:
   1. MAJOR version when you make incompatible API changes.
   2. MINOR version when you add functionality in a backwards-compatible manner, or make backwards-compatible bug fixes.

## about “incompatible API changes”

MAJOR does not need to be a factor if you’ve [properly deprecated something](Deprecation.md).

MAJOR does not need to be a factor if you’ve added, updated, removed, or promoted an [experimental feature](Experimental.md).

# See Also

- [FAQ](FAQ.md)
- [Changelog](CHANGELOG.md)
- [Semantic Versioning](http://semver.org/)
- We welcome feedback and discussion, please do so via the [git repository Issues](https://github.com/drmuey/simver/issues)

# License

[Creative Commons - CC BY 3.0](https://creativecommons.org/licenses/by/3.0/)
