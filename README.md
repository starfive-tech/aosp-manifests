AOSP Source Code Manifest for StarFive VisionFive v2 (JH7110 SoC)

# Setup build environment

Recommended setup:

Ubuntu 22.04.3 LTS (Jammy Jellyfish)

```
$ sudo apt-get install git-core gnupg flex bison build-essential zip curl zlib1g-dev libc6-dev-i386 libncurses5 x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig python3 python3-pip python3-setuptools python3-wheel ninja-build
```
```
$ sudo pip3 install meson
```
```
$ sudo pip3 install mako
```


# Getting AOSP source code

Create a workspace.
```
$ mkdir aosp && cd aosp
```

Initialize the workspace with the manifest file.
```
$ repo init -u https://github.com/starfive-tech/aosp-manifests.git -m default.xml
```

Clone the local manifest file for device specific source code.
```
$ git clone http://github.com/starfive-tech/starfive-manifests.git .repo/local_manifests -b jh7110-android14-v1.0
```

Sync to download the source code.
```
$ repo sync
```
