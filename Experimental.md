# Experimental Changes

There are basically two types. Short and long lived.

Aside from completely avoiding this particular rabbit hole here is a sane way to do them:

# Short Lived

Just do them in a branch and if it ends up being bad don't merge it up and if it ends up being good merge it up. Done.

# Long Lived

These are features you need to get you to the public for some real world battle scarring during an extended period of time.

To do this:

Add “EXEPERIMENTAL” to the “Types of changes” categories (in the “[Keep a Changelog](http://keepachangelog.com/en/1.0.0/)” format vernactular).

Always note, in your changelog, under “EXEPERIMENTAL” what was added Added, Changed, Removed or Promoted (also a new “Types of changes” that fits under EXPERIMENTAL) from experimental to mainline.

e.g.

```
…
### Added
- automatic cleanup of cache files on restart

### EXPERIMENTAL

#### Removed
- removed web socket API, its terribly broken and no one actually needs it

#### Promoted
- REST API for OAUTH2 authentication

…
```
