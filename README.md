# Archer C7 v2 builds

See branches of this repo.

## Usage

1. Install openwrt from the image at this repo.

2. Use custom opkg feeds:

   Configure `/etc/opkg/customfeeds.conf` with the following (replace `<branch>` with proper branch name):

   ```
   src/gz custom_openwrt_core https://github.com/MOZGIII/archer-c7-v2-builds/raw/<branch>/targets/ath79/generic/packages
   src/gz custom_openwrt_base https://github.com/MOZGIII/archer-c7-v2-builds/raw/<branch>/packages/mips_24kc/base
   src/gz custom_openwrt_luci https://github.com/MOZGIII/archer-c7-v2-builds/raw/<branch>/packages/mips_24kc/luci
   src/gz custom_openwrt_packages https://github.com/MOZGIII/archer-c7-v2-builds/raw/<branch>/packages/mips_24kc/packages
   src/gz custom_openwrt_routing https://github.com/MOZGIII/archer-c7-v2-builds/raw/<branch>/packages/mips_24kc/routing
   src/gz custom_openwrt_telephony https://github.com/MOZGIII/archer-c7-v2-builds/raw/<branch>/packages/mips_24kc/telephony
   ```
   
   > Alternatively, you can replace the official feeds by chaning the URLs at the `/etc/opkg/distfeeds.conf`. Keep in mind that not all branches contain full builds; you can consult `config.seed` to determine build parameters.

## Working on `master`

When cloning this repo to work on documentation at the `master` branch, use `--depth 1` argument to decrease the download volume.
