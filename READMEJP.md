[**中国語**](https://github.com/Miku-UI/manifesto/blob/TDA/READMECN.md)

# Miku UI TDA

![MikuUI](https://github.com/Miku-UI/manifesto/raw/TDA/img/MikuUI.png)

Miku UI は AOSP ベースのプロジェクトです。パフォーマンス面にフォーカスしているのが特徴です ... 

> **ミク？**

**始め方！**

えっと...キミはビルドボットなの？

それだったら始める前に [**Wiki**](https://github.com/Project-Mushroom/platform_manifest/wiki) をチェックしてね！

ソースコードの同期
------------


```shell
repo init -u https://github.com/Miku-UI/manifesto -b TDA
```


```shell
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```


## 気をつけてね

> Miku UI のビルドに ify-only-Device Configuration を使用している場合はリリースをしないでください。個人で使ってください。
>
> あなたの ify-only-Device Configuration を公開しないでください。元の作者を尊重してください、お願いします。
>
> また、ify-only-Device Configuration に基づいた Miku UI のビルドを Telegram チャンネルや XDA で公開しないでください。
> 
> 理由は Miku UI が不安定になり、問題を引き起こす可能性があるからです！

それがわかったら、その後は ...

## ビルド開始っ！！

```shell
# Init
. build/envsetup.sh

# Lunch
lunch miku_[codename]-[build type]

# Make a diva !
make diva
```


クレジット
-------
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**exTHmUI**](https://github.com/exthmui)
 * [**Weeb Project**](https://github.com/WeebProject)
 * [**Dirty Unicorns**](https://github.com/DirtyUnicorns)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**Mokee**](https://github.com/Mokee)
 * [**crDroid**](https://github.com/crdroidandroid)
