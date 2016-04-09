# README

## Installation

Pull the image `timonier/aria2`:

```sh
# Get the latest image (version 1.18.10)
docker pull timonier/aria2

# Or get a specific version

# Get the version 1.18.8
docker pull timonier/aria2:1.18.8
```

## Usage

Run the application via `docker run`. The [aria2 options](http://aria2.sourceforge.net/manual/en/html/aria2c.html) can be passed as arguments:

```sh
docker run \
    -i \
    -t \
    -v /data:/data \
    --net host \
    timonier/aria2 --dir=/data --enable-rpc --rpc-listen-all=true
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [aria2](http://aria2.sourceforge.net/)
* [aria2c options](http://aria2.sourceforge.net/manual/en/html/aria2c.html)
* [command "docker pull"](https://docs.docker.com/reference/commandline/pull/)
* [command "docker run"](https://docs.docker.com/reference/run/)
* [image "timonier/aria2"](https://hub.docker.com/r/timonier/aria2/)
