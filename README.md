# Miku UI

Miku UI是一个基于AOSP-CAF的系统。专注于性能优化与......

Miku？
-----

我要怎么开始捏？
-----------------------

首先，先确认好自己是否准备好了编译环境呢？

什么？你原来是个BuildBot吗！
---------------------------

嗯、问题不大~因为我们现在没有服务器，所以也很欢迎你成为Buildbot！

我们以Ubuntu20.04来做例子吧！

首先，在你的终端下面执行以下命令
```shell
sudo apt-get install python bc bison build-essential ccache curl flex g++-multilib gcc-multilib git gnupg gperf imagemagick lib32ncurses5-dev lib32readline-dev lib32z1-dev liblz4-tool libncurses5 libncurses5-dev libsdl1.2-dev libssl-dev libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc zip zlib1g-dev
```

这里我们做了什么呢？
------------------

通过上面这段命令，你将会部署好编译所需要的环境

那么接下来你要做的就是......

安装repo
---------

等等，什么事repo？
repo是一个方便的仓库管理工具,谷歌使用它来管理AOSP的源码，所以如果我们想要拉取AOSP源码的话，就需要安装这个工具哦！

在终端里执行

```shell
mkdir -p ~/bin
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
sudo cp ~/bin/repo /bin/repo
sudo chmod a+x /bin/repo
```
这下你就完成了repo的安装~！我们可以开始拉源码了吗！

替换镜像源
----------

你兴冲冲地做完以上步骤，认为可以开始拉源码了，但是你应该也知道，某咕噜咕噜在中国是被墙的状态哦。所以你需要有魔法才能拉取源码~
什么..？你没有魔法？

```
git config --global url.https://mirrors.bfsu.edu.cn/git/AOSP/.insteadof https://android.googlesource.com
git config --global url.https://github.com.cnpmjs.org/.insteadof https://github.com
```
在终端执行以上命令，就可以不用魔法来愉快地同步源码啦！


为MikuUI新建工作区！
------------------

虽然说、、直接在根目录同步源码也没什么问题。。但是真的不会觉得乱吗？
所以最好是，新建一个文件夹来放源码哦！

```shell
# 新建文件夹用来存放 Miku UI 源码
# ~/指用户目录
# 用户目录指 /home/用户名
# 此处的 Miku 为文件夹名，可自定义
mkdir ~/miku
cd ~/miku
```

同步源码
------------


终于到了这个步骤啦！接下来让我们来用repo来同步源码吧！

使用以下命令来初始化仓库:

    $    repo init -u https://github.com/Project-Mushroom/platform_manifest -b snow

开始同步源码:

    $    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```shell
# -j 参数为下载线程数，不带该参数默认自动分配线程
# -l 参数用于更新本地存储库
# --fail-fast 参数可以处理上次repo时由于网络原因导致的同步失败问题
#--force-sync 参数忽略本地修改，强制同步git仓库的内容。
```

开始编译！！
------------

准备好编译属于你的MikuUI了吗！让我们开始吧！
你需要做的有：

- 准备好“材料”（如果是自己写的那就太好了），也就是Device Configuration（或者叫Device Tree？）、Kernel Source（如果你使用预编译内核的话，请无视~）、Vendor Blobs（这个一般可以从手机里提取捏）

- 对现有的材料进行Ify（不推荐，如果你使用的是Ify的Device Configuration来编译MikuUI，那建议只供自己使用，不要发布，如果一定要发布的话，请注明Device Configuration的原作者！）

准备好了这些以后，让我们开始...

```shell
# 初始化编译环境
. build/envsetup.sh

# 初始化编译设备
lunch miku_[设备代号]-userdebug

# 开始编译属于你的Miku（Diva）！
make diva
```


特别鸣谢
-------
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**exTHmUI**](https://github.com/exthmui)
 * [**Weeb Project**](https://github.com/WeebProject)
 * [**Dirty Unicorns**](https://github.com/DirtyUnicorns)
