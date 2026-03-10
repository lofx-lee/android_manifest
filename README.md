# PixelOS

## Getting Started

To get started with the PixelOS source code, you'll need to be
familiar with [Git and Repo](https://source.android.com/setup/build/downloading).

To initialize your local repository, run:

```bash
repo init -u git@github.com:lofx-lee/android_manifest.git -b bp4a --git-lfs
```

Then, sync the repository:

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

## Building the System

Initialize the ROM build environment by sourcing the envsetup.sh script:

```bash
. build/envsetup.sh
```

After cloning the device-specific sources, use breakfast to configure the build for your device:

```bash
lunch custom_nuwa-bp4a-userdebug
```

Start the compilation:

```bash
mka pixelos -j$(nproc --all)
```

## Submitting Patches
Patches are always welcome! Feel free to submit your patches via [PixelOS Gerrit](https://review.pixelos.net/).
