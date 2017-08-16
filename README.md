# simver

Simple Versioning Specification 1.0

# Why?

Under this scheme, version numbers and the way they change convey *very little* meaning about the underlying code and what has been modified from one version to the next. That information is much better conveyed by a [proper changelog](http://keepachangelog.com/en/1.0.0/).

Some reasons why this is good:

1. comparing versions is now an extremely simple numeric operation
2. avoids most, if not all, potential confusion when basing decisions on data encoded in essentially 3 or 4 bits
3. builds and releases can still be tagged and referenced as needed
4. The data for properly measuring the impact of a version change can be found in the [proper changelog](http://keepachangelog.com/en/1.0.0/) entries between the version involved in the decision.
5. no special interpretation rules need to be applied or documented (0.x does not mean BETA, if its BETA say so in your marketing materials and changelog, even/odd does not mean dev/production, etc)

# Spec

1. Keep a [proper changelog](http://keepachangelog.com/en/1.0.0/). 
2. Given a version number MAJOR.MINOR, _on release_, increment the:
   1. MAJOR version when you make incompatible API changes.
   2. MINOR version when you add functionality in a backwards-compatible manner, or make backwards-compatible bug fixes.

## incompatible API changes

MAJOR does not need to be a factor if you’ve properly deprecated something.

MAJOR does not need to be a factor if you’ve added, updated, removed, or promoted an experimental feature.

## pre-release and build metadata

Additional labels for pre-release and build metadata _are not part of the version_. Instead you should denote those points in history by tags in your repository (displayed where appropriate for consumers) or whatever makes sense in your project. e.g.here is what your git tags may look like, + to denote builds and – to denote release candidate:
```
69c0232e v1.1
69c0232e –1236
69c0232e +1236
28793557, 
97c84b41 –1235
97c84b41 +1235
e3340037 +1234
b5377720 v1.0
```

Here we see after `v1.0` we had two changes, thought we we might have a release candidate (–1235), found a bug. Fixed it, built it (`+1236`), thought we we might have a release candidate (`–1235`), and sure enough it checked out so we released it (`v1.1`).

# Keep a Changelog

If you follow the [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) format you can make this change to their recommendation about referencing your use of Semantic Versioning:

```
- and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
+ and this project adheres to [Simple Versioning](https://drmuey.github.io/simver/).
```

# License

[Creative Commons - CC BY 3.0](https://creativecommons.org/licenses/by/3.0/)
