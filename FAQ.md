# Why?

Simpler is easier which means you are more likely to do it and it is more likely to be useful to your consumers.

Under this scheme, version numbers and the way they change convey *very little* meaning about the underlying code and what has been modified from one version to the next. That information is much better conveyed by a proper changelog (e.g. the “[Keep a Changelog](http://keepachangelog.com/en/1.0.0/)” format).

Some reasons why this is good:

1. comparing versions is now an extremely simple numeric operation (for computers and humans)
2. avoids most, if not all, potential confusion when basing decisions on data encoded in essentially 3± bits
3. builds and releases and disposition (e.g. beta, edge, public, stable, etc) can still be tagged and referenced as needed
4. The data for properly measuring the impact of a version change can be found in the proper changelog (e.g. the “[Keep a Changelog](http://keepachangelog.com/en/1.0.0/)” format) entries between the versions involved in the decision.
5. no special interpretation rules need to be applied or documented or programmed (0.x does not mean pre-release, if its BETA say so in your marketing materials and changelog, even/odd does not mean dev/production, etc)

For comparison see [Semantic Versioning](http://semver.org/). You may find it, or another version scheme, more suitable to your needs ¯\\_(ツ)_/¯.

# What about “pre-release and build metadata”?

Additional labels for pre-release and build metadata *are not part of the version*. Instead you should denote those points in history by tags in your repository (displayed where appropriate for consumers) or whatever makes sense in your project. e.g. here is what your git tags may look like, + to denote builds and – to denote release candidate (you could just as easily use “b” and “rc” as a prefix):
```
69c0232e v1.1
69c0232e –1236
69c0232e +1236
28793557
97c84b41 –1235
97c84b41 +1235
e3340037 
b5377720 v1.0
```

Here we see after `v1.0` we had two changes, thought we we might have a release candidate (–1235) and did a build (+1235), found a bug. Fixed it, built it (`+1236`), thought we we might have a release candidate (`–1236`), and sure enough it checked out so we released it (`v1.1`).

# What about about “disposition”?

If you want to convey which version beta, edge, stable, etc keep that mapping somewhere useful to your consumers.

That may be the changelog, it may be a release page, it may be a JSON file that code consumes, it may be git branches, etc.

The point is the version does not dictate the disposition of the code, the state of the code dictates the disposition of the version in question and its up to a human to decide if/how to map version to tiers based on context of the project.

# What do I do if I follow “Keep a Changelog” format?

If you follow the [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) format you can make this change to their recommendation about referencing your use of Semantic Versioning:

```diff
- and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
+ and this project adheres to [Simple Versioning](https://drmuey.github.io/simver/).
```
