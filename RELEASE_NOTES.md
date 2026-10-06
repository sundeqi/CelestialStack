# 月亮堆栈 0.3.1 公开测试版

适用于 Apple Silicon（M 系列）Mac，macOS 15 及以上。

## 提供的功能

- 扫描 RAW 文件夹，查看文件清单和读取问题。
- 自动选取参考照片，完成对齐与堆栈。
- 双窗同步查看单张与堆栈结果。
- 调节曝光、明暗对比、AI 降噪与锐化。
- 同时导出 16 位 TIFF 与最高质量 JPG。

## 本版更新

- 新增简体中文 / English 切换，覆盖欢迎页、任务设置及双窗编辑器。
- 自动记住语言选择，主窗口与编辑窗口同步。
- 切换语言时保留当前任务、拍摄间隔、路径及图像调整值。
- 新增英文使用指南。本次更新不改变堆栈和图像增强算法。

原始诊断日志保留原文；系统文件选择器的部分文字跟随 macOS 语言。

## 下载附件

- `MoonStack-0.3.1-public-beta-macOS15-arm64.dmg`：应用安装包及公开版说明。
- `月亮堆栈_用户使用说明书_公开测试版0.3.1.pdf`：安装与操作手册。
- `月亮堆栈_功能与兼容性说明_公开测试版0.3.1.pdf`：功能范围与已知限制。
- `MoonStack_User_Guide_0.3.1_Public_Beta.pdf`：英文使用指南。
- `SHA256SUMS.txt`：附件完整性校验值。

本仓库仅发布安装包及公开文档；GitHub 的 “Source code” 下载不包含应用源码。

## 已知限制

目前实拍验证主要来自 Sony ARW；其他品牌的具体机型与压缩模式需要更多样本验证。当前版本不支持 Windows、Intel Mac 或视频输入。

应用尚未完成 Apple Developer ID 签名和公证，首次启动可能受系统安全检查限制。取消计算不支持原地续算；已完成任务目录移动或改名后，重新打开可能失败。详情见用户手册。

欢迎通过 Issues 提交可复现的问题。反馈前请遮挡私人路径和照片信息。

## English

MoonStack 0.3.1 public beta is available for Apple Silicon Macs running macOS 15 or later. This release adds Simplified Chinese / English switching with a saved preference and synchronized windows. Switching language preserves the current task and image adjustments. The stacking and enhancement algorithms are unchanged.

Download the DMG below. The release also includes Chinese documentation, an English user guide and SHA256 checksums. GitHub's automatically generated source archives contain only public documentation, not the application source code.

The app is not Developer ID signed or notarized. Real-photo testing has focused on Sony ARW; other camera and compression combinations need further validation. See the user guides for first-launch instructions and current limitations.
