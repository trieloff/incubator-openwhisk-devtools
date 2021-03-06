Developer tools for OpenWhisk
=============================

This repository is part of [Apache OpenWhisk](http://openwhisk.org) and provides developer tools that help with local development, testing and operation of OpenWhisk.

## Subprojects

* [docker-compose](docker-compose/README.md) allows testing OpenWhisk locally, using Docker Compose. This is ideal if you are contributing to core development
* [kubernetes](kubernetes/README.md) is a work in progress to allow local testing on a Kubernetes cluster.
* [node-local](node-local/README.md) allows testing individual OpenWhisk functions locally, using only node.js. This is ideal if you are writing node.js functions to run in OpenWhisk, but need to emulate some of OpenWhisk's behavior in creating `params` and expecting promises.

## Travis builds

Each tool in this repository has to provide travis build scripts inside a `.travis` folder. 
The folder should define 2 scripts:
* `setup.sh` - invoked during `before_install` phase 
* `build.sh` - invokes during `script` phase 

For an example check out [docker-compose/.travis](docker-compose/.travis) folder.
