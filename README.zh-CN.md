# Highway2Hell

[English](README.md) · 中文 · [日本語](README.ja.md)

Highway2Hell 是下载网络视频和音频的桌面应用。它是 [yt-dlp](https://github.com/yt-dlp/yt-dlp)（一个免费的命令行下载工具）的图形界面，不用敲命令就能用。

## 下载与安装

打开 [Releases 页面](https://github.com/Ishtar-Gate/h2h-releases/releases)。最上面带「Latest」标记的是最新版本，在它下方的 **Assets**（下载文件列表）里下载对应系统的文件：

| 系统 | 文件 |
|---|---|
| Windows | 文件名以 `_x64-setup.exe` 结尾的 |
| macOS（Apple 芯片，M1 及以后），未经测试 | 文件名以 `_aarch64.dmg` 结尾的 |
| macOS（Intel 芯片），未经测试 | 文件名以 `_x64.dmg` 结尾的 |
| Linux，未经测试 | 文件名以 `.AppImage` 结尾的（也可以用 `.deb` / `.rpm`） |

不知道自己的 Mac 是哪种芯片时，点屏幕左上角的苹果图标，选「关于本机」：「芯片」一栏写着 Apple M1、M2 这样的是 Apple 芯片，「处理器」一栏写着 Intel 的是 Intel 芯片。

Linux 上 `.AppImage` 在大多数发行版上都能直接运行；`.deb` 用于 Ubuntu、Debian，`.rpm` 用于 Fedora 等。拿不准就选 `.AppImage`。

macOS 和 Linux 版还没有经过测试。遇到问题请按下面「反馈问题」里的方法告诉我们。

打开下载的文件，按安装程序的提示操作。不需要自己安装 yt-dlp：第一次启动时，应用会自己下载需要的程序。只有 macOS 和 Linux 上的 ffmpeg 要自己安装，见下面的[下载组件没法自动安装时](#下载组件没法自动安装时)。

有新版本时应用会提示你，你确认后它会自动安装。

## 下载组件没法自动安装时

Highway2Hell 下载时要用到几个单独的程序，界面上统称「下载组件」：

- **yt-dlp**：读取视频信息并下载。
- **ffmpeg**：把画面和声音合成一个文件、转换格式。
- **deno**：下载部分 YouTube 视频时 yt-dlp 需要它。

一般情况下，应用会自己下载安装这些程序。有时没法自动安装，这时应用会告诉你哪个程序要自己装：

- 在 macOS 和 Linux 上，ffmpeg 要自己安装。
- 少数类型的电脑上，yt-dlp 或 deno 也可能要自己安装。

按各程序官方的说明安装：

- ffmpeg：[官方下载页](https://ffmpeg.org/download.html)
- yt-dlp：[官方安装说明](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
- deno：[官方安装说明](https://docs.deno.com/runtime/getting_started/installation/)

官方说明里有好几种装法。请选用软件安装工具来装：macOS 上是 Homebrew（Mac 上常用的一个免费软件安装工具），Linux 上是系统自带的软件包管理器（例如 Ubuntu 的 apt）。这样装好后，应用就能找到它。如果只是下载了程序文件、放进某个文件夹，应用找不到它。

装好后回到应用：

- ffmpeg、yt-dlp：在应用提示你安装的那一页点「重新检测」。
- deno：在「关于」页点「重新检测」。

## 支持的网站

yt-dlp 支持的网站都可以下载，完整的列表见 yt-dlp 的[支持网站列表](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md)。

## 反馈问题

在[这里](https://github.com/Ishtar-Gate/h2h-releases/issues/new/choose)新建一个 issue（GitHub 上的问题反馈）。需要有 GitHub 账号。

先按内容选一种表单：Bug report（问题反馈）、Feature request（功能需求）、Translation（翻译）或 Other（其他）。表单是英文的，内容用中文填写也可以。

方便的话请附上诊断信息：在应用里点侧栏底部的「关于」，再点「导出诊断信息」，在弹出的窗口里选好保存的位置，会保存一个 `.zip` 文件，把它拖进 issue 的输入框即可。诊断信息不含 Cookie，代理密码等敏感内容也已打码。旁边的「反馈问题」按钮会直接打开 Bug report 表单。

## 声明

Highway2Hell 本身不存储也不分发任何媒体内容。请只下载你有权保存的内容，并遵守所在地区的法律和各网站的服务条款。本软件不提供绕过付费或 DRM（数字版权保护）的功能。
