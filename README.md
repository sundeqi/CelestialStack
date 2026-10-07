# 月亮堆栈 MoonStack

简体中文 | [English](README.en.md)

MoonStack 是一款面向月亮摄影的 RAW 堆栈工具，支持自动选帧与对齐、双窗对比，以及曝光、明暗对比、AI 降噪和锐化调节。照片在本机处理，可同时导出 16 位 TIFF 和最高质量 JPG，支持简体中文与英文界面。

MoonStack is a lunar RAW stacking app with automatic frame selection and alignment, side-by-side comparison, and exposure, contrast, AI denoising and sharpening controls. Process photos locally and export 16-bit TIFF and maximum-quality JPG, with a Simplified Chinese or English interface.

**当前为 0.3.1 公开测试版，仅提供安装包和用户文档，暂不公开应用源码。**

## 界面预览

![CelestialStack 0.3.4 英文界面：增加留白后的单张与堆栈对比](assets/celestialstack-compare-export-en-v034.png)

CelestialStack（原 MoonStack）0.3.4 新版预览：使用 12 张实际 RAW 重新堆栈，月亮周围留白在 0.3.3 基础上再增加 25%（裁切尺寸向上取整）。左侧为未调整的最佳单张，右侧为堆栈后调整效果；两侧以相同倍率显示完整构图（降噪 0%、锐化 100%、对比度 40%、曝光 +0.0 EV）。新版安装包尚未上传 Releases，当前公开下载版本见下方说明。

## 下载与安装

进入本仓库的 [Releases](https://github.com/sundeqi/MoonStack/releases) 页面，选择标记为 **Pre-release** 的公开测试版本，在附件中下载 macOS 安装包。GitHub 自动生成的 “Source code” 压缩包仅包含本仓库的公开文档，不是应用程序。

打开 DMG，将“月亮堆栈.app”拖入“应用程序”，再从应用程序文件夹启动。具体步骤见[用户使用说明书](docs/用户使用说明书.md)。

## 系统与素材

| 项目 | 说明 |
|---|---|
| 电脑 | Apple Silicon（M 系列）Mac |
| 系统 | macOS 15 及以上；目前实机验证为 macOS 15.8.1 |
| 照片 | 同一拍摄组，至少 10 张可读取的 RAW |
| 输入格式 | Sony ARW、Nikon NEF、Panasonic RW2、Canon CR2 / CR3 / CRW |
| 输出 | 16 位 TIFF、最高质量 JPG，可同时导出 |

Sony ARW 已进行实拍验证；其他格式的具体机型、压缩模式仍在收集测试反馈。扩展名支持不等于所有相机组合均已验证。当前安装包不适用于 Intel Mac 或 Windows。

## 快速开始

1. 选择 RAW 文件夹并扫描。
2. 填写拍摄间隔（未知可留空），选择输出目录。
3. 保留默认设置，检查任务后开始堆栈。
4. 完成后打开双窗编辑器，在相同位置和倍率下查看单张与堆栈结果。
5. 调整右图，导出 TIFF、JPG 或两者。

## 界面语言

欢迎页、主界面及编辑器右上角均可切换“简体中文 / English”。默认简体中文，选择会自动保存；切换时保留当前任务、图片与调整值。原始诊断日志保留原文，系统文件选择器的部分文字跟随 macOS 语言。

## 测试版须知

照片在本机处理，原始 RAW 不会被覆盖。请保留原片与重要成片。

当前安装包尚未使用 Apple Developer ID 签名及完成公证，首次打开可能受到系统安全检查限制。请核对发布页校验值，并参考 [Apple 的首次打开说明](https://support.apple.com/zh-cn/102445)；不要关闭系统整体安全保护。

堆栈效果受原片对焦、抖动、大气条件、曝光与可用照片数量影响，不保证每组素材都比最佳单张具有更高的真实分辨率。调整过强也可能导致颗粒、光晕或纹理变平。

完整功能及限制见[功能与兼容性说明](docs/功能与兼容性说明.md)。

## 反馈

欢迎通过本仓库 Issues 提交问题。请提供应用版本、Mac 型号与系统版本、相机型号、RAW 格式与压缩模式、照片数量、复现步骤及简短错误信息。截图和错误信息请先遮挡用户名、完整路径和其他私人信息；无需公开原始照片或整个任务目录。

## 支持开发 / Support MoonStack

如果 MoonStack 对你有帮助，欢迎自愿打赏，支持后续开发与维护。If MoonStack is useful to you, consider leaving a voluntary tip to support continued development.

**USDT · TRON（TRC20）**

```text
TYuBQ5Rij9z7SddmyDyHz3ErzabeAUnnAT
```

[查看收款二维码与说明 / View QR code and instructions](docs/SUPPORT.md)

[在 B 站为我充电 / Support me on Bilibili](https://b23.tv/fRtpz7l) · 打开个人主页后选择“充电”。

打赏完全自愿，不影响当前公开测试版的使用，也不代表购买未来付费功能。Tips are optional and do not purchase a license for future paid features.

## 授权与第三方组件

本项目采用闭源分发方式，公开测试不等于开源授权。自有程序与文档保留权利，第三方组件按各自许可证提供。详见[公开测试与版权说明](COPYRIGHT.md)及安装包附带的第三方声明。
