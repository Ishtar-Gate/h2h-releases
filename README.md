# Highway2Hell

English · [中文](README.zh-CN.md) · [日本語](README.ja.md)

A desktop app for downloading online videos and audio. It is a graphical interface for [yt-dlp](https://github.com/yt-dlp/yt-dlp), a free command-line downloader, so you can use it without typing commands.

## Download and install

Open the [Releases page](https://github.com/Ishtar-Gate/h2h-releases/releases). The version at the top marked "Latest" is the newest one; under it, in **Assets** (the list of download files), download the file for your system:

| System | File |
|---|---|
| Windows | the file ending in `_x64-setup.exe` |
| macOS (Apple silicon, M1 and later), untested | the file ending in `_aarch64.dmg` |
| macOS (Intel), untested | the file ending in `_x64.dmg` |
| Linux, untested | the file ending in `.AppImage` (or `.deb` / `.rpm`) |

If you don't know which chip your Mac has, click the Apple menu in the top-left corner and choose **About This Mac**: if **Chip** shows Apple M1, M2 and so on, it is Apple silicon; if **Processor** shows Intel, it is Intel.

On Linux, the `.AppImage` runs directly on most distributions; `.deb` is for Ubuntu and Debian, `.rpm` for Fedora and similar. If unsure, choose the `.AppImage`.

The macOS and Linux versions have not been tested yet. If something does not work, please report it as described in [Reporting a problem](#reporting-a-problem) below.

Open the downloaded file and follow the installer. You do not need to install yt-dlp yourself: on first launch the app downloads the programs it needs. Only ffmpeg on macOS and Linux has to be installed by you; see [If download tools can't be installed automatically](#if-download-tools-cant-be-installed-automatically) below.

When a new version is out, the app tells you, and it installs the update after you confirm.

## If download tools can't be installed automatically

Highway2Hell uses a few separate programs to download, called "download tools" in the app:

- **yt-dlp** reads video info and downloads.
- **ffmpeg** combines picture and sound into one file and converts formats.
- **deno** is needed by yt-dlp for some YouTube videos.

Usually the app downloads and installs these programs itself. When it can't, the app tells you which program to install yourself:

- On macOS and Linux, you install ffmpeg yourself.
- On a few kinds of computers, you may also need to install yt-dlp or deno yourself.

Install them by following each program's official instructions:

- ffmpeg: [official download page](https://ffmpeg.org/download.html)
- yt-dlp: [official installation guide](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
- deno: [official installation guide](https://docs.deno.com/runtime/getting_started/installation/)

The official instructions offer several ways to install. Please use a software installer: on macOS that is Homebrew (a free tool commonly used to install software on a Mac); on Linux it is your system's package manager (for example apt on Ubuntu). Installed this way, the app can find the program. If you only download the program file and put it in some folder, the app cannot find it.

When done, go back to the app:

- ffmpeg, yt-dlp: click **Check again** on the page where the app asked you to install it.
- deno: click **Check again** on the **About** page.

## Supported sites

Highway2Hell can download from any site yt-dlp supports. See yt-dlp's [list of supported sites](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md).

## Reporting a problem

Create a new issue (a problem report on GitHub) [here](https://github.com/Ishtar-Gate/h2h-releases/issues/new/choose). You need a GitHub account.

First pick the form that fits: Bug report, Feature request, Translation, or Other.

If you can, attach diagnostics: in the app, click **About** at the bottom of the sidebar, then **Export diagnostics**, and choose where to save it in the window that opens. This saves a `.zip` file; drag it into the issue's text box. Diagnostics contain no cookies, and proxy passwords and other sensitive values are masked. The **Report a problem** button next to it opens the Bug report form directly.

## Disclaimer

Highway2Hell does not store or distribute any media. Only download content you have the right to keep, and follow the laws of your region and each site's terms of service. It does not bypass paywalls or DRM (copy protection).
