### Installation

Pull the image `mauchede/wiremock`:

```bash
# Get the latest image
docker pull mauchede/wiremock

# Or get a specific version

# Get the version 1.57
docker pull mauchede/wiremock:1.57
```

### Usage

Run your container via `docker run`. The [wiremock options](http://wiremock.org/running-standalone.html) can be passed as arguments. For example:

```bash
docker run --name wiremock mauchede/wiremock:1.57 -v --port 80
```

### Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

### Links

* [command "docker pull"](https://docs.docker.com/reference/commandline/pull/)
* [command "docker run"](https://docs.docker.com/reference/run/)
* [image "mauchede/wiremock"](https://hub.docker.com/r/mauchede/wiremock/)
* [wiremock](http://wiremock.org/)
* [wiremock options](http://wiremock.org/running-standalone.html)
