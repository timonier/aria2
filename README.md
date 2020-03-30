# README

High speed download utility

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://gitlab.com/timonier/aria2/raw/master/bin/installer" | sudo bash -s -- install
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

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a [merge request](https://docs.gitlab.com/ee/user/project/merge_requests/).

__Note__: [GitHub repository](https://github.com/timonier/aria2) is a mirror. [Merge request](https://docs.gitlab.com/ee/user/project/merge_requests/) has to be submitted to the [GitLab repository](https://gitlab.com/timonier/aria2).

If you like / use this project, please let me known by adding a [★](https://help.github.com/articles/about-stars/) on the [GitHub repository](https://github.com/timonier/aria2) or on the [GitLab repository](https://gitlab.com/timonier/aria2).

## Links

* [aria2/aria2](https://github.com/aria2/aria2)
* [image "timonier/aria2"](https://hub.docker.com/r/timonier/aria2/)
* [set up docker for mac with native nfs](https://medium.com/@sean.handley/how-to-set-up-docker-for-mac-with-native-nfs-145151458adc)
* [timonier/version-lister](https://gitlab.com/timonier/version-lister)
