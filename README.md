# Installation

Pull the image `timonier/aria2`:

```bash
# Get the latest image
docker pull timonier/aria2

# Or get a specific version

# Get the version 1.18.8
docker pull timonier/aria2:1.18.8
```

# Usage

Run your container via `docker run`. The [aria2 options](http://aria2.sourceforge.net/manual/en/html/aria2c.html) can be passed as arguments:

```bash
docker run -it --net=host -v /data:/data timonier/aria2 --dir=/data --enable-rpc --rpc-listen-all=true
```

# Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

# Links

* [aria2](http://aria2.sourceforge.net/)
* [aria2c options](http://aria2.sourceforge.net/manual/en/html/aria2c.html)
* [command "docker pull"](https://docs.docker.com/reference/commandline/pull/)
* [command "docker run"](https://docs.docker.com/reference/run/)
* [image "timonier/aria2"](https://hub.docker.com/r/timonier/aria2/)
