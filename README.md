# Syosetu Translate Releases

这是 Syosetu Translate 的公开发布与应用更新仓库。Android 源码保存在私有仓库中；这里仅发布签名 APK、更新清单和公开发布说明。

## 安装包

- 正式版包名：`com.wearshoes.syosetu`
- 当前版本：`0.1.0`（`versionCode 1`）
- 最低 Android 版本：Android 8.0（API 26）
- 下载入口：[GitHub Releases](https://github.com/wearshoes/syosetu-releases/releases)

Debug 包使用独立包名 `com.wearshoes.syosetu.debug`，只用于本地开发调试，不在此仓库公开发布。Debug 与正式版可以同时安装。

## 应用更新

应用从 [`latest.json`](latest.json) 获取最新正式版本。该清单提供版本号、APK 下载地址、发布页面、SHA-256 和发布时间。更新采用完整签名 APK 覆盖安装，不使用动态 DEX 或运行时代码注入。

正式版后续更新必须继续使用同一签名证书，并确保 `versionCode` 单调递增，否则 Android 不允许覆盖安装。

## 完整性校验

下载 APK 后可计算 SHA-256，并与 `latest.json` 的 `sha256` 字段比较：

```powershell
Get-FileHash .\syosetu-v0.1.0.apk -Algorithm SHA256
```

## 说明

这是非官方个人阅读客户端。小说正文由原站页面加载，本仓库不收录或再发布小说内容。LLM 服务凭据由用户在设备上提供，不包含在 APK 或本仓库中。
