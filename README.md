This module makes testing of RHMAP components easier by running a build jobs with [s2i](https://github.com/openshift/source-to-image) (source2image) and [fh-npm](https://www.npmjs.com/package/fh-npm) tools.

`fh-build`'s main purpose is to be installed as a tool in CI testing, e.g. in [Travis CI](http://travis-ci.org).

It contains a shell script installing couple of dependencies:
- npm@2.13.5 for node v4, or npm@3.10.8 for node v6 or npm@5.6.0 for node v8
- [grunt-cli](https://www.npmjs.com/package/grunt-cli)
- [fh-npm](https://www.npmjs.com/package/fh-npm)
- [s2i](https://github.com/openshift/source-to-image)
- [golang](https://github.com/golang/go)

It also assumes you have a [docker](https://www.docker.com/) running locally.

## Install
`$ npm install fh-build -g`

The module is meant to be used globally. Running it as a dependency module was not properly tested yet.

## Usage
Go to the repository folder you want to build and run:

`$ fh-build <build-type>`

- \<build-type\> - currently only `template` type

## Compatibility
It is adjusted to the Travis CI testing environment (currently Ubuntu 14.04.3 LTS) and running it on a different OS could be problematic.
