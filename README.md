# Packer Build: Raspberry Pi Image

Build Raspberry Pi images using Docker and Packer.

Enabling SSH on raspbian requires creating a `/boot/ssh` file. `raspbian.json`
creates the file and a [goss](https://github.com/aelsabbahy/goss) test
validates it exists.

## Requirements

- docker
- docker-compose

## Usage

Checkout git submodules.

```sh
git submodule update --init --recursive
```

Build `raspbian.img`

```sh
make build
```

The `raspbian.img` artifact can be burned to an SD card. I
use [etcher](https://www.balena.io/etcher) for burning.
