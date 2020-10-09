# README

A web service test double for all occasions

If you like / use this project, please let me known by adding a ★ on the [GitHub repository](https://github.com/timonier/wiremock).

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://github.com/timonier/wiremock/raw/master/bin/installer" | sudo sh -s -- install
```

__Note 1__: If you do not define `INSTALL_DIRECTORY`, `installer` will use in `/usr/local/bin`.

__Note 2__: `docker-for-mac` users have to configure [native NFS server](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc).

## Usage

Run the command `wiremock`:

```sh
# See all wiremock options

wiremock --help

# Run wiremock

wiremock --root-dir /tmp --verbose
```

## Links

* [image "timonier/wiremock"](https://hub.docker.com/r/timonier/wiremock/)
* [set up docker for mac with native nfs](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc)
* [timonier/wiremock](https://github.com/timonier/wiremock)
* [tomakehurst/wiremock](https://github.com/tomakehurst/wiremock)
