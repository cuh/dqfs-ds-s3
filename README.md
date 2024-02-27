# S3 Datastore Implementation

This is an implementation of the datastore interface backed by amazon s3.

**NOTE:** Plugins only work on Linux and MacOS at the moment. You can track the progress of this issue here: https://github.com/golang/go/issues/19282

## Quickstart

  1. Grab a plugin release from the [releases](https://github.com/ipfs/go-ds-s3/releases) section matching your Kubo version and install the plugin file in `~/.ipfs/plugins`.
  2. Follow the instructions in the plugin's [README.md](go-ds-s3-plugin/README.md)


## Building and installing


The plugin can be manually built/installed for different versions of Kubo (starting with 0.23.0) with:

```
git checkout go-ds-s3-plugin/v<kubo-version>
make plugin
make install-plugin
```

## Updating to a new version

  1. `go get` the Kubo release you want to build for. Make sure any other
     dependencies are aligned to what Kubo uses.
  2. `make install` and test.


If you are building against dist-released versions of Kubo, you need to build using the same version of go that was used to build the release ([here](https://github.com/ipfs/distributions/blob/master/.tool-versions)).

If you are building against your own build of Kubo you must align your plugin to use it.

If you are updating this repo to produce a new version of the plugin:
