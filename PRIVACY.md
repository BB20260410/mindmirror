# MindMirror 隐私政策

**最后更新：2026-05-18**

MindMirror（Lite 与 Pro 版本统称"本软件"）是一款 macOS 桌面应用，由独立开发者维护。本隐私政策说明本软件如何处理你的数据。

## 1. 我们收集什么数据

**屏幕截图与 OCR 文本**

- 本软件需要"屏幕录制"权限定期截屏（默认每秒抓帧）
- 截图经本地 Apple Vision OCR 转文本
- **截图与 OCR 文本不上传到任何远端服务器**
- 仅 OCR 文本的**摘要**（通常 < 2000 字符）会被发送给你**自己配置**的 LLM 服务商

**LLM API 调用**

- 你在设置中配置的 LLM 服务商（MiniMax、Anthropic、自定义 OpenAI 兼容）会收到：
  - 屏幕 OCR 摘要
  - 你的主目标文本
  - 项目上下文（你自己写的 system prompt 补充）
- LLM 服务商各自的隐私政策适用：
  - [MiniMax 隐私政策](https://www.minimaxi.com/privacy)
  - [Anthropic 隐私政策](https://www.anthropic.com/privacy)

**项目元数据**

- 项目名、主目标、工作目录路径、月预算等存于 macOS 本地 `~/Library/Application Support/MindMirror/`
- 不上传

**API Key**

- 所有 API Key 存于 **macOS Keychain**（系统加密保护）
- 不上传

## 2. 我们不收集

- ❌ 个人身份信息（姓名、邮箱、电话等）—— 本软件不要求注册
- ❌ 浏览器历史 / 文件系统遍历
- ❌ 麦克风 / 摄像头
- ❌ 位置信息
- ❌ 任何形式的 telemetry / analytics

## 3. 第三方数据共享

本软件**不与任何第三方共享你的数据**，除非：

1. 你**主动配置**了某个 LLM 服务商（数据按上述 §1 发送给该服务商）
2. 你**主动开启**了 Hermes Agent MCP 桥集成（Hermes Agent 可读取 MindMirror 状态，但 Hermes 本身也运行在你本地）
3. 你**主动开启**了通知集成（Bark / Ntfy / Slack / Feishu webhook），通知内容发到你配置的 URL

## 4. 数据存储位置

- **macOS Keychain**：API Key（系统加密）
- **`~/Library/Application Support/MindMirror/`**：项目配置、时间轴、思维导图、本地 RAG 索引
- **`~/Library/Caches/MindMirror/`**：临时截图缓存（自动清理）
- **`~/Library/Logs/MindMirror/`**：调试日志（用户可手动清理）

## 5. 你的权利

- **导出**：设置 → 配置 → 导出全部数据为 JSON
- **删除**：卸载本软件 + 删除上述目录即可完全清除
- **撤回 LLM 调用**：在设置中清空 API Key 即停止任何 LLM 通信

## 6. 儿童

本软件不面向 13 岁以下儿童，且不主动收集任何用户的年龄信息。

## 7. 变更通知

本政策若有重大变更，会通过软件内 banner 公告。建议偶尔回访本页面查看更新时间。

## 8. 联系

- 邮件：ilifelahepeq54@gmail.com
- GitHub Issue：https://github.com/BB20260410/mindmirror/issues

---

**法律管辖**：本政策受中华人民共和国法律管辖，但本软件遵守购买地区适用的消费者保护法（如 GDPR、CCPA）。
