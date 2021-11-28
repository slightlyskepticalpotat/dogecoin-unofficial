Here are all the commands for building and uploading to the Snap Store. Snapcraft's CI system builds and tests .snap packages on amd64 (x86_64), arm64 (aarch64), and i386 (i686), so users on those architectures can install the latest version from the Snap Store (see below). That is the recommended way to install dogecoin-unofficial. Users can also manually build and install dogecoin-unofficial with the commands below, or download and install one of the older .snap packages from this repository.

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

## Usage
```
dogecoin-unofficial.cli # for dogecoin-cli
dogecoin-unofficial.d # for dogecoind
dogecoin-unofficial.qt # for dogecoin-qt
dogecoin-unofficial.tx # for dogecoin-tx
dogecoin-unofficial.test # for test_dogecoin
```

## Uninstalling
```
sudo snap remove dogecoin-unofficial
```
