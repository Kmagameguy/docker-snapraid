# Build Snapraid in a Docker Container

[![CI](https://github.com/Kmagameguy/docker-snapraid/actions/workflows/ci.yml/badge.svg)](https://github.com/IronicBadger/docker-snapraid/actions/workflows/ci.yml)

This container will allow you to build a Snapraid `.deb` file without installing any build dependencies on your system.

### Pre-Requisites
You will need a working copy of [docker][docker] to build the container.

### Usage

```sh
./build.sh [<version>] # e.g. ./build.sh 11.5
sudo dpkg -i snapraid*.deb
```

If the version is omitted, the latest version of SnapRAID is used.

The build script spins up a container, executes the `Dockerfile` which performs the actual build from source. The script then copies the built `.deb` artifact out onto your local system ready for installation using `dpkg`.

To save building it yourself, you can also download the `.deb` file as an artifact from GitHub actions.

[docker]:https://docs.docker.com/engine/install/
