# aria2

Dockerized [aria2](http://aria2.sourceforge.net/): High speed download utility.

## Installation

Copy the script `bin/aria2c` into your executable folder (like `/usr/local/bin` or `$HOME/bin`).

```bash
sudo curl -sLo /usr/local/bin/aria2c https://github.com/mauchede/aria2/raw/master/bin/aria2c
sudo chmod +x /usr/local/bin/aria2c
```

## Usage

Run the script `aria2c`:

```bash
aria2c --dir=/data --enable-rpc --rpc-listen-all=true
```

__Note__: By default, the version `1.18.8` will be used. To change the version, define the `TAG` before the command. For example:

```bash
TAG="latest" ariac -v
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

## Links

* [aria2c options](http://aria2.sourceforge.net/manual/en/html/aria2c.html)
* [command "docker run"](https://docs.docker.com/reference/run/)
* [image "mauchede/aria2"](https://hub.docker.com/r/mauchede/aria2/)
