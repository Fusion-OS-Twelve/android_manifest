![FusionOS](extras/FusionBanner.png)

### Requirements
- Around 200G disk space.
- A computer/server with at least 16GB RAM running Linux.
- Some brain cells.

### Instructions
1. Make sure you have a build environment setup.

### Sync ###
```bash
        repo init -u https://github.com/Fusion-OS/android_manifest -b twelve
        repo sync --current-branch --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j$(nproc --all)

```

### GAPPS ###
Usage of GAPPS is optional
```bash
WITH_GAPPS := true
```
### Build ###
```bash
        source build/envsetup.sh
        lunch fuse_$device-userdebug
        make fuse-prod -j$(nproc --all)
```

Submitting Patches
==================
>> Fusion-OS is an open source project thus any patches/contributions are always welcome !

>> To begin with, you need to login to our code review system at [FusionOS Code Review](https://review.gerrithub.io/q/project:Fusion-OS/)

>> We support login using Github Oauth provider, which means if you have either of account you can login to gerrit by that account.
It is important that you set the USERNAME in your account on gerrit. If you have logged in using Github account then your Github USERNAME will be used as gerrit USERNAME automatically. Else you can set unique username in `Profile` section of gerrit account Settings.

>> The next step is to add your SSH key to your gerrit account.

>> Refer the Github guide on [how to generate SSH key](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

>> Add the generated SSH key (the contents of id_rsa.pub file) to your gerrit account in `SSH Public Keys` section.


>> You can upload the patches/contributions for review process using following procedure:

- [Always make sure to clone from FusionOS github]

```bash
      $ git clone 
```

>> For Example -  git clone https://github.com/Fusion-OS/android_packages_apps_Settings.git

```bash
      $ cd CLONED_DIRECTORY
```

>> Make the changes you wish to add for review and execute following commands,

```bash
      $ git add -A
      $ git commit -m "commit message"
```

>> Commit message should be clear, well written and easy to understand.

>> If you have satisfied with the changes you made then you can upload the patchset to gerrit.

```bash
      $ git push ssh://username@review.gerrithub.io:29418/Fusion-OS/<repo_name> HEAD:refs/for/<branch>
```

>> Here the PROJECT_NAME is the path to repository on gerrit. You can find the PROJECT_NAME by navigating to the `Projects` section on gerrit.

>> For example - android_packages_apps_Settings

>> It is recommended that you commit your several relevent patches in to one single commit.

>> Squash multiple commits using this command:

```bash
      $ git rebase -i HEAD~<# of commits>
```

>> If you are going to make extra changes to an existing patch, Don't start a new patch, instead

```bash
      $ git add .
      $ git commit --amend
```
>> and simply push the changes to gerrit

>> Gerrit will recognize it as a new patchset in an exisiting commit.

>> To view the status of your and/or others patches, visit [FusionOS Code Review](https://review.gerrithub.io/q/project:Fusion-OS/)

Credits
-------
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**AOSPA**](https://github.com/AOSPA)
 * [**HentaiOS**](https://github.com/hentaios)
 * [**Weeb Project**](https://github.com/weebproject)
 * [**Paranoid Android**](https://github.com/AOSPA)
 * [**Project Radiant**](https://github.com/ProjectRadiant)
 * [**StormbreakerOSS**](https://github.com/StormbreakerOSS)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**StyxOS**](https://github.com/stxyproject)
 * [**Pixel Experience**](https://github.com/PixelExperience)
 * And the list never ends.
