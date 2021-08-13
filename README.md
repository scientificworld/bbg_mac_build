# BBG macOS构建 on GitHub

如题。

构建方法（macOS版）：

```bash
git clone https://gitee.com/baiyang-lzy/bbg.git
cd bbg
npm install electron-packager -g # 如果已经安装过可忽略此步
npm install electron
cp icons/icon.ico icons/icon.icns
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
