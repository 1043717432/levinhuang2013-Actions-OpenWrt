**English** | [中文](https://p3terx.com/archives/build-openwrt-with-github-actions.html)

# Actions-OpenWrt

[![LICENSE](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square&label=LICENSE)](https://github.com/P3TERX/Actions-OpenWrt/blob/master/LICENSE)
![GitHub Stars](https://img.shields.io/github/stars/P3TERX/Actions-OpenWrt.svg?style=flat-square&label=Stars&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/P3TERX/Actions-OpenWrt.svg?style=flat-square&label=Forks&logo=github)

A template for building OpenWrt with GitHub Actions

## Usage

- Click the [Use this template](https://github.com/P3TERX/Actions-OpenWrt/generate) button to create a new repository.
- Generate `.config` files using [Lean's OpenWrt](https://github.com/coolsnowwolf/lede) source code. ( You can change it through environment variables in the workflow file. )
- Push `.config` file to the GitHub repository.
- Select `Build OpenWrt` on the Actions page.
- Click the `Run workflow` button.
- When the build is complete, click the `Artifacts` button in the upper right corner of the Actions page to download the binaries.

## Tips

- It may take a long time to create a `.config` file and build the OpenWrt firmware. Thus, before create repository to build your own firmware, you may check out if others have already built it which meet your needs by simply [search `Actions-Openwrt` in GitHub](https://github.com/search?q=Actions-openwrt).
- Add some meta info of your built firmware (such as firmware architecture and installed packages) to your repository introduction, this will save others' time.

## Credits

- [Microsoft Azure](https://azure.microsoft.com)
- [GitHub Actions](https://github.com/features/actions)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [coolsnowwolf/lede](https://github.com/coolsnowwolf/lede)
- [Mikubill/transfer](https://github.com/Mikubill/transfer)
- [softprops/action-gh-release](https://github.com/softprops/action-gh-release)
- [Mattraks/delete-workflow-runs](https://github.com/Mattraks/delete-workflow-runs)
- [dev-drprasad/delete-older-releases](https://github.com/dev-drprasad/delete-older-releases)
- [peter-evans/repository-dispatch](https://github.com/peter-evans/repository-dispatch)
- 云编译7981固件 （p3terx 2024新版 基于ubuntu22.04）

360T7主路由固件，含插件DDNS, PASSWALL（用最新源码编译）。

JCG Q30 PRO极简AP固件。

237大佬源码网址: https://github.com/padavanonly/immortalwrt-mt798x-24.10

passwall最新源码网址： https://github.com/xiaorouji/openwrt-passwall

ssr plus最新源码网址： https://github.com/fw876/helloworld

使用p3terx云编译模板 English | 中文

config配置文件，建议采用本地生成。可装linux或者Windows下装wsl，按照官方编译步骤操作。

要使用passwall最新源码，需要更改feeds.conf.default，文件开始处插入：

src-git passwall_packages https://github.com/xiaorouji/openwrt-passwall-packages.git;main
src-git passwall https://github.com/xiaorouji/openwrt-passwall.git;main
注意，新建的repositories ，要修改权限（原来只读，改成读写权限）。

Settings，Actions，General，右侧栏拉到最下面， Workflow permissions，勾选 Read and write permissions

更新刷写固件时，跨版本更新的，记得不要保存设置。

刷写完新固件后，记得先清理浏览器缓存，再访问路由器进行设置。

## License

[MIT](https://github.com/P3TERX/Actions-OpenWrt/blob/main/LICENSE) © [**P3TERX**](https://p3terx.com)
