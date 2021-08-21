All the commands I used for building and pushing to Snapcraft. I've only tested the amd64 .snap package, but anyone on amd64, arm64, or i686 should be able to build and/or install it for themselves with these instructions.

---

## Installing From Snap Store

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/dogecoin-unofficial)

[![dogecoin-unofficial](https://snapcraft.io/dogecoin-unofficial/badge.svg)](https://snapcraft.io/dogecoin-unofficial)

## Building Locally

```
sudo apt install snapd
sudo snap install --classic snapcraft
snapcraft
```

### To Install Locally
```
snap install \*.snap --devmode
```

### To Push to Snapcraft
```
snapcraft login
snapcraft register dogecoin-unofficial
snapcraft push \*.snap --release=edge
sudo snap install dogecoin-unofficial --channel=edge
```