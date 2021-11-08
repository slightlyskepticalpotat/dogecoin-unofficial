Here are all the commands I use for building and pushing to Snapcraft. I've only tested the amd64 (x86_64) and arm64 (aarch64) .snap packages, but anyone on amd64 (x86_64), arm64 (aarch64), or i686 (i386) should be able to build and install the snap themselves with these instructions.

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

### To Push to Snapcraft
```
snapcraft login
snapcraft register dogecoin-unofficial
snapcraft push \*.snap
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
