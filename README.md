[**中文版**](https://github.com/Miku-UI/manifesto/blob/Udon/READMECN.md) | [**日本語**](https://github.com/Miku-UI/manifesto/blob/Udon/READMEJP.md)

# Miku UI Udon

![MikuUI](https://github.com/Miku-UI/manifesto/raw/Udon/img/MikuUI.png)

Miku UI is an AOSP-Based Project focus on Performance and ... 

> **Miku？**

**How to Start！**

Well...Are you a buildbot?

Then, check [**Our Wiki**](https://github.com/Miku-UI/manifesto/wiki) before you start！

Sync Sourcecode
------------


```shell
repo init -u https://github.com/Miku-UI/manifesto -b Udon
```


```shell
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
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
lunch miku_[codename]-[build type]

# Make a diva !
make diva
```
