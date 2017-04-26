# README

High speed download utility

## Installation

Copy `bin/aria2c` into your executable folder (like `/usr/local/bin` or `$HOME/bin`):

```sh
sudo curl --location --output /usr/local/bin/aria2c "https://github.com/timonier/soffice/raw/master/bin/aria2c"
sudo chmod +x /usr/local/bin/aria2c
```

Linux users can use the [installer](https://github.com/timonier/aria2c/blob/master/bin/installer):

```sh
curl --location "https://github.com/timonier/aria2c/raw/master/bin/installer" | sudo sh -s install
```

## Usage

Run the command `aria2c`:

```sh
# See all aria2c options

aria2c --help

# Run aria2c

aria2c --dir /data --enable-rpc --rpc-listen-all
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [aria2/aria2](https://github.com/aria2/aria2)
* [image "timonier/aria2"](https://hub.docker.com/r/timonier/aria2/)
* [timonier/dumb-entrypoint](https://github.com/timonier/dumb-entrypoint)
* [timonier/version-lister](https://github.com/timonier/version-lister)
