# README

A web service test double for all occasions

## Installation

Copy `bin/wiremock` into your executable folder (like `/usr/local/bin` or `$HOME/bin`):

```sh
sudo curl --location --output /usr/local/bin/wiremock "https://github.com/timonier/wiremock/raw/master/bin/wiremock"
sudo chmod +x /usr/local/bin/wiremock
```

Linux users can use the [installer](https://github.com/timonier/wiremock/blob/master/bin/installer):

```sh
curl --location "https://github.com/timonier/wiremock/raw/master/bin/installer" | sudo sh -s install
```

## Usage

Run the command `wiremock`:

```sh
# See all wiremock options

wiremock --help

# Run wiremock

wiremock --root-dir /tmp --verbose
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [image "timonier/wiremock"](https://hub.docker.com/r/timonier/wiremock/)
* [timonier/dumb-entrypoint](https://github.com/timonier/dumb-entrypoint)
* [timonier/version-lister](https://github.com/timonier/version-lister)
* [tomakehurst/wiremock](https://github.com/tomakehurst/wiremock)
