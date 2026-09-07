# 变更日志 (Changelog)

本项目遵循 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/) 规范，版本格式采用 [Semantic Versioning](https://semver.org/lang/zh-CN/)。

---

## [1.1.3] - 2026-09-07

### 🔧 修复与优化 (Fixed & Changed)
- **修正商汤日日新 / 智子星 (SenseNova) 官方入口**：
  - 将限时免费专区及结构化数据中商汤科技的官方链接全面修正为官方主页：`https://www.sensenova.cn/`。
  - 同步更新 `data/providers.json` 与 `data/models.json` 中商汤日日新的官方网站及相关入口。
- **外部链接全面支持新页面打开**：
  - 将主文档 `README.md` 及相关配置手册中所有外部官网、API Key 申请和控制台跳转链接统一重构为 `<a href="..." target="_blank" rel="noopener noreferrer">` 格式。
  - 点击外部链接时均在新标签页中打开，大幅提升开发者在 GitHub 浏览时的导航体验，避免离开当前仓库。
- **版本与全量校验更新**：
  - `data/providers.json` 全局版本升级至 `1.1.3`，校验时间更新至 `2026-09-07`。
  - `data/models.json` 全局版本升级至 `1.1.3`，校验时间更新至 `2026-09-07`。
  - `README.md` 徽章与最后校验日期同步更新至 `1.1.3` 与 `2026-09-07`。

---

## [1.1.2] - 2026-09-03

### 🚀 新增 (Added)
- **新增中国移动 (移动云 MaaS 墨玛大模型广场) 平台**：
  - **平台与厂商**：中国移动 / 移动云 (China Mobile ECloud)
  - **重点模型**：`DeepSeek-V4-Flash-0731`（最新一代超低时延、2840亿参数规模 MoE 旗舰模型）
  - **免费额度**：新开通/体验即**免费赠送 2500 万 Tokens** 大额度资源包
  - **官方入口**：`https://ecloud.10086.cn/api/page/maas/moma/modelSquare`
  - **状态**：`🟡 有免费额度`
- **更新场景推荐与快速入口**：
  - 在“🔥 当前最值得领取”与“💻 Coding 编程”中推荐移动云与 DeepSeek-V4-Flash-0731。
  - 在主页快速入口与平台详细档案中补充移动云直达链接与参数。
- **扩展结构化数据**：
  - `data/providers.json` 扩充至 17 家厂商/平台，全局版本升至 `1.1.2`。
  - `data/models.json` 扩充至 26 款模型数据，全局版本升至 `1.1.2`。

---

## [1.1.1] - 2026-09-03

### 📌 规约确立 (Policy)
- **版本号递增规约**：正式确立规则——每当收录并发布一个新的模型、厂商或重点福利内容时，版本号补丁位固定递增 `0.0.1`（遵循语义化版本规范，从 `1.1.0` 升级至 `1.1.1`）。

### 🚀 新增 (Added)
- **🔥 限时免费：智谱 GLM 编码计划与 ZCode (ZCodeX) ADE 桌面环境**：
  - **平台与厂商**：Z.ai / 智谱 AI
  - **重点模型**：`GLM-5.3-Flash`（320B 总参/18B 稀疏激活原生多模态编程大模型）
  - **活动时间**：2026年9月3日 至 9月20日
  - **时段规则**：每天太平洋时间 08:00 至 18:00（即 **北京时间每天 23:00 至次日 09:00**）
  - **福利力度**：
    1. **在官方 ZCode 桌面端内**：活动时段内完全无限制免费使用 `GLM-5.3-Flash`（Unlimited）
    2. **在第三方支持的代理（Cursor、Claude Code、Cline 等）中**：活动期间直接享受 **2x Flash 配额（双倍额度）**
  - **官方入口**：`https://z.ai`
  - **状态**：`🔥 限时免费`
- **更新 AI 编程手册**：
  - 在 `docs/coding-tools.md` 中新增第 7 节：ZCode 智能体桌面端与 GLM 编码计划实战配置指南。
- **扩展结构化数据**：
  - `data/providers.json` 扩充至 16 家厂商/平台，全局版本升至 `1.1.1`。
  - `data/models.json` 扩充至 25 款模型数据，全局版本升至 `1.1.1`。

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
