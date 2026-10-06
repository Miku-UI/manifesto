[**中国語**](https://github.com/Miku-UI/manifesto/blob/Cinderella/READMECN.md)

# Miku UI Cinderella

![MikuUI](https://github.com/Miku-UI/manifesto/raw/Cinderella/img/MikuUI.webp)

Miku UI は AOSP ベースのプロジェクトです。パフォーマンス面にフォーカスしているのが特徴です ... 

> **ミク？**

**始め方！**

えっと...キミはビルドボットなの？

それだったら始める前に [**Wiki**](https://github.com/Miku-UI/manifesto/wiki) をチェックしてね！

ソースコードの同期
------------


```shell
repo init -u https://github.com/Miku-UI/manifesto -b Cinderella --git-lfs
```


```shell
repo sync -c --force-sync --no-clone-bundle --no-tags
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

### Miku UI Build System TUI を試してみよう！

完全にグラフィカルなビルドインターフェースです。ぜひ試してみてください！
Miku UI のソースコードのルートディレクトリで、以下を実行します：

```shell
./build_miku.py
```

エラーが発生したり、起動できなかったりする場合は、必要な依存関係がすべてインストールされているか確認してください！
Miku UI Build System TUI が要求する Python の最低バージョンは 3.9 です。

#### 依存関係のインストール

```shell
sudo apt-get update
sudo apt-get install -y \
  python3 \
  python3-curses \
  libncursesw6 \
  ncurses-term \
  bash \
  locales \
  git \
  git-lfs \
  ccache \
  xclip \
  wl-clipboard
```

### 従来の方法

```shell
# Init
. build/envsetup.sh

# Lunch
lunch miku_[codename]-[release]-[build type]

# Make a diva !
make diva
```

## GSI ビルドガイド（古い内容です。Miku UI Build System TUI を使用してください）

ソースコードを変更していない限り、いつでも Miku UI の GSI イメージをビルドすることができます。そうしてビルドされた GSI は、公式サーバーでコンパイルされた GSI（署名を除く）と完全に同一になります！

常に最新の変更を体験したい場合は、ぜひ 手動でビルドしてみてください〜

ここでは、ARM64 スマートフォン向けの GSI ビルドを例に説明します。
対応しているその他のバリエーションについては、[こちらをご覧ください](https://github.com/Miku-UI/manifesto/wiki/English-Wiki#about-gsi-build-target)
。

```shell
# Init
. build/envsetup.sh

# Lunch
lunch miku_gsi_phone_arm64-[release]-[build type]

# Make GSI !
make systemimage
```
