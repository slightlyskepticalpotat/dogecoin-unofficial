All the commands I used for building and pushing to Snapcraft. I've only pushed the amd64 .snap package, but anyone on amd64, arm64, or i686 should be able to build it for themselves with these instructions.

---

## Building Locally

sudo apt install snapd
sudo snap install --classic snapcraft
snapcraft

### To Install Locally
snap install \*.snap --devmode

### To Push to Snapcraft
snapcraft login
snapcraft register dogecoin-unofficial
snapcraft push \*.snap --release=edge
sudo snap install dogecoin-unofficial --channel=edge
