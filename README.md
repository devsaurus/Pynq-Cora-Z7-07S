# Pynq-Cora-Z7-07S [![GitHub Release](https://img.shields.io/github/v/release/devsaurus/Pynq-Cora-Z7-07S?include_prereleases)](https://github.com/devsaurus/Pynq-Cora-Z7-07S/releases)

Pre-built SD card image can be downloaded from the [release assets](https://github.com/devsaurus/Pynq-Cora-Z7-07S/releases).

## Build inside docker

Install tools and docker as per https://pynq.readthedocs.io/en/latest/pynq_sd_card.html

This repo must be accessible from within the docker container. E.g. clone it in `/workspace`.

`make BOARDDIR=<path to this repo>`

### Missing python modules

If python modules are missing, simply install them in the container:

```shell
sudo apt-get update
sudo apt-get diffstat
sudo apt-get lz4 zstd
sudo pip3 install PyYAML
```

### Download/fetch fails

Simple run `make ...` again.

### Device tree compile error

Copy `PYNQ/system-top.dts` from this repo to `/workspace/PYNQ/sdbuild/build/Pynq-Cora-Z7-07S/petalinux_project/components/plnx_workspace/device-tree/device-tree/`.
