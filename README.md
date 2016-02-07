# Installation

Pull the image `timonier/wiremock`:

```bash
# Get the latest image
docker pull timonier/wiremock

# Or get a specific version

# Get the version 1.57
docker pull timonier/wiremock:1.57
```

# Usage

Run your container via `docker run`. The [wiremock options](http://wiremock.org/running-standalone.html) can be passed as arguments:

```bash
docker run --name wiremock timonier/wiremock:1.57 -v --port 80
```

# Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

# Links

* [command "docker pull"](https://docs.docker.com/reference/commandline/pull/)
* [command "docker run"](https://docs.docker.com/reference/run/)
* [image "timonier/wiremock"](https://hub.docker.com/r/timonier/wiremock/)
* [wiremock](http://wiremock.org/)
* [wiremock options](http://wiremock.org/running-standalone.html)
