# README

High speed download utility

If you like / use this project, please let me known by adding a ★ on the [GitHub repository](https://github.com/timonier/aria2).

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://github.com/timonier/aria2/raw/master/bin/installer" | sudo bash -s -- install
```

__Note 1__: If you do not define `INSTALL_DIRECTORY`, `installer` will use in `/usr/local/bin`.

__Note 2__: `docker-for-mac` users have to configure [native NFS server](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc).

## Usage

Run the command `aria2c`:

```sh
# See all aria2c options

aria2c --help

# Run aria2c

aria2c --dir /data --enable-rpc --rpc-listen-all
```

## Links

* [aria2/aria2](https://github.com/aria2/aria2)
* [image "timonier/aria2"](https://hub.docker.com/r/timonier/aria2/)
* [set up docker for mac with native nfs](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc)
* [timonier/aria2](https://github.com/timonier/aria2)
