[**中文版**](https://github.com/Miku-UI/manifesto/blob/Blooming/READMECN.md) | [**日本語**](https://github.com/Miku-UI/manifesto/blob/Blooming/READMEJP.md)

# Miku UI Blooming

![MikuUI](https://github.com/Miku-UI/manifesto/raw/Blooming/img/MikuUI.webp)

Miku UI is an AOSP-Based Project focus on Performance and ... 

> **Miku？**

**How to Start！**

Well...Are you a buildbot?

Then, check [**Our Wiki**](https://github.com/Miku-UI/manifesto/wiki) before you start！

Sync Sourcecode
------------


```shell
repo init -u https://github.com/Miku-UI/manifesto -b Blooming --git-lfs
```


```shell
repo sync -c --force-sync --no-clone-bundle --no-tags
```


## Be Careful

> If you are using an ify-only-Device Configuration for building Miku UI , DO NOT RELEASE IT, FOR OWN USE ONLY.
>
> And please DO NOT Public your ify-only-Device Configuration, respect the original author, plz.
>
> DO NOT RELEASE any build of Miku UI based on an ify-only-Device Configuration to any telegram channel or XDA Forum.
> 
> Bcz it's unstable with Miku UI and may lead problems!

After that let's ...

## Start to build！！

```shell
# Init
. build/envsetup.sh

# Lunch
lunch miku_[codename]-[release]-[build type]

# Make a diva !
make diva
```

## GSI Building Guide

You can build a GSI image at any time, and as long as you haven't modified the source code, it will be identical to the GSI compiled from the official server (except for the signature)!

If you want to experience the latest changes immediately, then compile it manually!

The following guide is for arm64 phone, more available selections [check here](https://github.com/Miku-UI/manifesto/wiki/English-Wiki#about-gsi-build-target)

```shell
# Init
. build/envsetup.sh

# Lunch
lunch miku_gsi_phone_arm64-[release]-[build type]

# Make a diva !
make diva
```
