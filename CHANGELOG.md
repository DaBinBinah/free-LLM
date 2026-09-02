# 变更日志 (Changelog)

本项目遵循 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/) 规范，版本格式采用 [Semantic Versioning](https://semver.org/lang/zh-CN/)。

---

## [1.1.0] - 2026-09-02

### 🚀 新增 (Added)
- **🔥 限时免费专区**：在 README 首屏核心位置新增“⚠️ 限时免费说明”与“🔥 当前限时免费”专区。
- **新增 3 家中国平台实测免费模型入口**：
  1. **商汤日日新 (SenseNova)**：
     - 模型：`GLM / K3`
     - 额度：约 60 万积分免费额度
     - 入口：`https://sensenova.cn/models`
     - 状态：`🟡 有免费额度`
  2. **AMD 开发者平台**：
     - 模型：`DeepSeek V4 Flash`
     - 额度：当前完全免费体验
     - 入口：`https://developer.amd.com.cn`
     - 状态：`🔥 限时免费`
  3. **华为云 CodeArts / 码道**：
     - 模型：`GLM5.3Flash`
     - 额度：每人每天免费赠送 1000 万 Tokens
     - 入口：`https://activity.huaweicloud.com/codearts_agent.html`
     - 状态：`🔥 限时免费`
- **更新场景速选 (🚀 不知道选哪个？)**：
  - 增加【🔥 当前最值得领取】限时福利推荐项。
  - 在【💻 Coding】场景中补充 AMD 与华为云高规格限时备选推荐。
  - 在【✍️ 通用中文】场景中补充商汤 GLM / K3 推荐。
- **扩展结构化数据**：
  - `data/providers.json` 扩充至 15 家厂商/平台。
  - `data/models.json` 扩充至 24 款模型数据。

---

## [1.0.0] - 2026-09-02

### 🌟 项目初始化与架构建立 (Initial Release)
- **项目定位确立**：打造专为中国大陆用户量身定制的“🇨🇳 中国免费大模型 API 大全”开源导航与知识库。
- **核心筛选原则**：
  - 严格只收录中国本土大模型厂商与境内直连平台。
  - 严格剔除海外中转/代理平台（如 OpenRouter、Groq、Together AI 等）。
  - 严格区分“开源模型”与“免费 API”，杜绝虚假与模糊信息。
- **建立 5 类免费状态标准**：
  - 🟢 长期免费
  - 🟡 有免费额度
  - 🟠 新用户免费
  - 🔴 已停止
  - ⚪ 待确认
- **首发收录 12 家主流平台与 21 款精选模型**：
  - 魔搭社区 (ModelScope)、智谱 AI (BigModel)、硅基流动 (SiliconFlow)、百度千帆、讯飞星火、阿里云百炼 (DashScope)、DeepSeek 官方、火山引擎 (豆包)、月之暗面 (Kimi)、MiniMax、无问芯穹、零一万物。
- **交付文档与工具体系**：
  - `README.md` & `README.zh-CN.md`：精简直观的首页、推荐榜、快速入口、完整模型档案。
  - `docs/openai-compatible.md`：Python / TypeScript / cURL / LangChain 标准接入代码与 Base URL 踩坑指南。
  - `docs/coding-tools.md`：Cursor、Claude Code、Codex CLI、Cline、OpenCode、Aider 6 大 AI 编程工具详细配置手册。
  - `data/providers.json` & `data/models.json`：全量结构化 JSON 数据库。
  - `CONTRIBUTING.md` & `LICENSE`：贡献准则与 MIT 开源许可证。
