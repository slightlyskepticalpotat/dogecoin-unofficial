# dogecoin-unofficial
Here are the commands for building and uploading a Dogecoin Core Snap to the Snap Store. Snapcraft's CI system builds and tests .snap packages on amd64 (x86_64) and arm64 (aarch64), so users on those architectures can install the latest version from the Snap Store. That is the recommended way to install dogecoin-unofficial. Users can also manually build and install dogecoin-unofficial or download and install one of the older .snap packages from this repository. Due to GitHub's file size limits, some `.snap` files are stored in [multipart](https://unix.stackexchange.com/questions/40480/how-to-unzip-a-multipart-spanned-zip-on-linux) `.zip` archives.

i386 (i686) support ended at 1.14.6 due to Snap limitations. If your architecture is 32-bit, use is not recommended.

---

## Snap Store Installation
[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/dogecoin-unofficial)
[![dogecoin-unofficial](https://snapcraft.io/dogecoin-unofficial/badge.svg)](https://snapcraft.io/dogecoin-unofficial) [![dogecoin-unofficial](https://snapcraft.io/dogecoin-unofficial/trending.svg?name=0)](https://snapcraft.io/dogecoin-unofficial)
```
sudo snap install dogecoin-unofficial
```

## Building Locally
```
sudo apt install snapd
sudo snap install --classic snapcraft
snapcraft
```

### Installing Locally
```
snap install \*.snap --devmode
```

### To Upload to the Snap Store
```
snapcraft login
snapcraft register dogecoin-unofficial
snapcraft upload \*.snap
sudo snap install dogecoin-unofficial
```
To push to and install from the `edge` channel, append `--release=edge` to the `upload` and `--channel=edge` to the `install` commands.

## Usage
```
dogecoin-unofficial.cli # for dogecoin-cli
dogecoin-unofficial.d # for dogecoind
dogecoin-unofficial.qt # for dogecoin-qt
dogecoin-unofficial.test # for test_dogecoin
dogecoin-unofficial.tx # for dogecoin-tx
```

## Updating
```
sudo snap refresh dogecoin-unofficial
```
Unless disabled, automatic updates take place whenever there is a new stable release.

## Uninstalling
```
sudo snap remove dogecoin-unofficial
```
To remove all user data, add `--purge`. Be careful, as this will delete your `wallet.dat` file.
