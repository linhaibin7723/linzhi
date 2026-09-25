# 手机免费编译 APK（GitHub Actions）

## 1. 注册/登录 GitHub
手机浏览器打开 https://github.com/ ，注册或登录账号。

## 2. 新建仓库
右上角 + → New repository。
仓库名例如：FakeOCAT。
选择 Public，Create repository。

## 3. 上传源码
进入刚创建的仓库 → Add file → Upload files。
把本项目解压后的 **FakeOCAT-main 文件夹里的全部内容**上传到仓库根目录。
注意：不要把 FakeOCAT-main 再套一层，否则 Actions 找不到 gradlew。

## 4. 开启 Actions
进入仓库 → Actions。
如果 GitHub 提示需要允许 Actions，点允许。
左侧选择 **Build APK** → **Run workflow** → **Run workflow**。

## 5. 下载 APK
等待工作流变成绿色成功。
打开这次运行 → 页面底部 Artifacts → 下载 **FakeOCAT-debug-apk**。
下载的是 zip，解压后里面有 `app-debug.apk`。

## 6. 手机上安装
点击 `app-debug.apk` 安装。如果 Android 提示禁止安装未知来源，按系统提示允许当前浏览器/文件管理器安装即可。

## 注意
- 每次你把新代码推送到 main/master，也会自动编译一次。
- 这个工作流生成的是 debug APK，不需要签名密钥，最适合个人手机测试。
- GitHub Actions 免费额度和限制会随账号类型、仓库可见性及 GitHub 规则变化。
