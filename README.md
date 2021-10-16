### Requirements
- Around 200G disk space.
- A computer/server with at least 16GB RAM running Linux.
- Some brain cells.

### Instructions
1. Make sure you have a build environment setup.

### Sync ###
```bash
        repo init -u https://github.com/fusionos-next/android_manifest -b twelve
        repo sync --current-branch --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j$(nproc --all)

```

### Build ###
```bash
        source build/envsetup.sh
        lunch fuse_$device-userdebug
        make fuse-prod -j$(nproc --all)
```

Credits
-------
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**HentaiOS**](https://github.com/hentaios)
 * [**Weeb Project**](https://github.com/weebproject)
 * [**Paranoid Android**](https://github.com/AOSPA)
 * [**Project Radiant**](https://github.com/ProjectRadiant)
 * [**StormbreakerOSS**](https://github.com/StormbreakerOSS)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**StyxOS**](https://github.com/stxyproject)
 * [**Pixel Experience**](https://github.com/PixelExperience)
 * And the list never ends.
