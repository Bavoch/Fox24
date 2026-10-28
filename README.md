# Fox24

免费的跨平台 24 帧动画桌面工作台。

**[下载安装包 →](https://github.com/Bavoch/Fox24/releases)**

- 使用本机 Codex CLI 润色创意和生成动画帧图。
- 导入 6×4 精灵图、24 帧预览与微调。
- 导出 GIF、动画 WebP 或视频。
- 保存 `.fox24` 工程，恢复上次工作。
- 没有 Fox24 账户、积分或付费功能，不接入产品云 API。

## 下载

| 系统 | 安装包 |
| --- | --- |
| macOS Apple Silicon | `mac-arm64.dmg` 或 `.zip` |
| macOS Intel | `mac-x64.dmg` 或 `.zip` |
| Windows 64 位 | `win-x64.exe` |
| Linux 64 位 | `linux-x86_64.AppImage` 或 `linux-amd64.deb` |

Ubuntu 24.04 等限制用户命名空间的系统建议使用 `.deb`，安装器会配置沙箱与 AppArmor。AppImage 需要系统允许用户命名空间。

从 [Releases](https://github.com/Bavoch/Fox24/releases) 选择对应版本与文件。每个版本附带 `SHA256SUMS.txt`。

当前为候选版本，macOS 使用 ad-hoc 签名，尚未完成 Apple Developer ID 公证；Windows 未签名。系统可能提示未知开发者。请自行核实来源与校验值。尚未完成所有系统与实体设备的安装验收。

## AI 使用准备

安装 Node.js，然后在终端运行：

```sh
npm install -g @openai/codex
codex login
```

使用 ChatGPT 登录，CLI 版本要求 `0.164.0` 或更新。打开 Fox24 后点击「连接 Codex」并重新检测。也可以手动选择 Codex 可执行文件。Windows 使用原生 Codex 安装，不需要运行网页 Bridge。

Fox24 本身免费。AI 使用用户自己的 ChatGPT 账户，仍需要互联网并受账户资格、用量和原生生图支持限制；这不是离线模型，也不是无限免费 AI 服务。Fox24 不读取或复制登录凭据，不接受 API Key。仅导入、编辑、预览与导出已有图片无需登录。

## 隐私与数据

图片处理、工程和自动恢复都保存在本机。生成时提示词和参考图会经本机 Codex 交给其服务。Fox24 不自建 AI 云后端，不收集遥测。Codex 保留生成图的位置由 CLI 自己管理。

这是安装包发布仓库，源码仓库和开发历史保持私有。免费使用不等同于开放源码授权。
