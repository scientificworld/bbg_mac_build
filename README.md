# BBG macOS构建 on GitHub

如题。

目前最新版本为`20210817`，下载地址：<https://github.com/scientificworld/bbg_mac_build/releases/download/20210817/bbg-darwin-x64.zip>

构建之前，请先看一下原仓库的[开发环境搭建指南](https://gitee.com/baiyang-lzy/bbg/blob/master/Docs/Developer_Guide.md)

构建方法（macOS版）：

```bash
git clone https://gitee.com/baiyang-lzy/bbg.git
cd bbg
npm install electron-packager -g # 如果已经安装过可忽略此步
npm install electron
# cp icons/icon.ico icons/icon.icns
# 上一步由于原仓库已修改所以不需要了
rm -r bbg-darwin-x64
cnpm run package_darwin 
```

另外，如果本地已经有仓库（且依赖项均已安装）：

```bash
cd /path/to/bbg
rm -r bbg-darwin-x64
git add .
git stash
git pull
cnpm run package_darwin
```
