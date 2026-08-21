# Syosetu Translate Releases

**中文** | [English](README.en.md)

这是 Syosetu Translate 的公开发布与应用更新仓库。Android 源码保存在私有仓库中；本仓库只发布签名、压缩后的正式版 APK、`release-manifest.json`、`latest.json` 和公开更新日志。

## 下载与安装

- 正式版包名：`com.wearshoes.syosetu`
- 最低系统：Android 8.0（API 26）
- 下载入口：[GitHub Releases](https://github.com/wearshoes/syosetu-releases/releases)
- 最新版本信息：[`latest.json`](latest.json)

Debug 包名为 `com.wearshoes.syosetu.debug`，只用于本地调试，不会上传到本仓库。Debug 与正式版可同时安装。

## 应用更新

应用读取 `latest.json` 检查新版本，并在更新弹窗中显示与 GitHub Release 完全一致的中文更新日志。`latest.json` 是面向 Android 客户端的兼容投影；每个 Release 同时附带标准 `release-ops/release-manifest/v1` 格式的 `release-manifest.json`。

正式版必须始终使用同一签名证书并递增 `versionCode`，Android 才允许覆盖安装。

## 完整性校验

```powershell
Get-FileHash .\syosetu-vX.Y.Z.apk -Algorithm SHA256
```

计算结果应与 `latest.json.sha256` 一致。每个公开 Release 只能包含一个正式 APK，不能包含 Debug APK。

本项目是非官方个人阅读客户端。小说正文由原站加载，本仓库不收录或再发布小说内容。LLM API Key 由用户在设备上配置，不包含在 APK 或本仓库中。
