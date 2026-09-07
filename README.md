<div align="center">

# 🇨🇳 中国免费大模型 API 大全 (free-LLM)

> **专为中国开发者打造的免费大模型 API 导航与开源知识库**  
> 精选中国本土大模型厂商与国内直连 AI 平台提供的永久免费 API、免费模型与限时免费额度。  
> 拒绝海外套壳，拒绝把“开源模型”硬当“免费 API”，一手官方真实数据，开箱即用。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version: 1.1.3](https://img.shields.io/badge/Version-1.1.3-green.svg)](CHANGELOG.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Last Verified](https://img.shields.io/badge/Last%20Verified-2026--09--07-orange.svg)](#-平台与模型详细档案)
[![OpenAI Compatible](https://img.shields.io/badge/OpenAI-Compatible%20100%25-green.svg)](docs/openai-compatible.md)

[🔥 限时免费](#-当前限时免费) · [🌟 推荐](#-推荐) · [🚀 场景速选](#-不知道选哪个) · [🔑 快速入口](#-中国免费-api-快速入口) · [⚡ OpenAI 兼容调用](#-openai-compatible) · [💻 AI 编程配置](#-ai-coding-编程工具配置) · [📊 完整清单](#-平台与模型详细档案)

</div>

---

## 📌 核心收录原则与免费定义

本项目**只收录中国本土厂商和中国境内直接可访问的官方模型平台**（如魔搭社区、智谱 AI、硅基流动、阿里云百炼、百度千帆、讯飞星火、DeepSeek 等）。

### 🏷️ 免费状态标识说明

- 🟢 **长期免费**：官方明确长期/永久免费商用，或每日/每月固定重置免费调用额度（无过期作废限制）。
- 🟡 **有免费额度**：开通赠送固定额度包或按模型赠送免费调用量（通常有 30~90 天有效期）。
- 🟠 **新用户免费**：新注册或首次实名认证赠送一次性体验代金券/Token 额度包。
- 🔴 **已停止**：此前提供过免费 API，当前已下线或转为全付费。
- ⚪ **待确认**：官方政策处于过渡期或暂无法从官方渠道明确确认。

---

## ⚠️ 限时免费说明

> 本项目特别收录部分限时免费活动。  
> “限时免费”不代表永久免费，活动可能提前结束、调整额度或改变使用条件。  
> 本项目维护者会尽量根据实际测试更新状态，但最终以官方页面及实际使用情况为准。

---

## 🔥 当前限时免费

> 经过实测确认可用的限时高额度福利，活动可能随时变动，建议尽快领取使用：

| 平台 / 厂商 | 重点模型 | 免费额度 / 说明 | 状态 | 官方入口 | 特别说明 |
| :--- | :--- | :--- | :---: | :---: | :--- |
| **Z.ai / ZCode<br>(智谱 GLM 编码计划)** | GLM-5.3-Flash | **限时时段完全无限制**<br>第三方代理 **2x 配额** | 🔥 限时 | <a href="https://z.ai" target="_blank" rel="noopener noreferrer">官方网站 →</a> | ⚡ **重磅福利（9月3日~9月20日）**：每天太平洋时间 08:00~18:00（**北京时间 23:00~次日 09:00**），在官方 ZCode ADE 桌面端内**无限制免费使用 GLM-5.3-Flash**；在其他支持的编程代理（Cursor、Claude Code、Cline 等）中享受 **2x Flash 配额**！ |
| **商汤日日新 / 智子星 (SenseNova)** | GLM / K3 | **约 60 万积分** 免费额度 | 🟢 免费额度 | <a href="https://platform.sensenova.cn/" target="_blank" rel="noopener noreferrer">官方平台 →</a> | 当前平台提供约 60 万积分免费额度，可使用 GLM、K3 等模型；免费政策可能调整，请以官方页面为准。 |
| **AMD 开发者** | DeepSeek V4 Flash | **当前免费** | 🔥 限时 | <a href="https://developer.amd.com.cn" target="_blank" rel="noopener noreferrer">官方网站 →</a> | ⚠️ 限时免费：当前可免费使用 DeepSeek V4 Flash，活动可能随时结束，建议尽快领取。 |
| **华为云 CodeArts / 码道** | GLM5.3Flash | 每天 **1000 万 Tokens** | 🔥 限时 | <a href="https://activity.huaweicloud.com/codearts_agent.html" target="_blank" rel="noopener noreferrer">官方活动 →</a> | ⚡ 限时活动：每人每天免费赠送 1000 万 Tokens，可使用 GLM5.3Flash。活动规则可能调整，请以华为云官方页面为准。 |

---

## ⭐ 推荐

| 模型名称 | 平台 / 厂商 | 免费状态 | 免费额度 / 说明 | 上下文 | OpenAI Compatible |
| :--- | :--- | :---: | :--- | :---: | :---: |
| **Qwen2.5-Coder-32B-Instruct** | <a href="https://www.modelscope.cn" target="_blank" rel="noopener noreferrer">魔搭社区 (ModelScope)</a> | 🟢 长期免费 | **每日 2000 次** 免费 API-Inference 极速调用 | 128K | ✅ 是 |
| **GLM-4-Flash** | <a href="https://open.bigmodel.cn" target="_blank" rel="noopener noreferrer">智谱 AI 开放平台</a> | 🟢 长期免费 | **永久免费商用**，128K 超大上下文，高并发 | 128K | ✅ 是 |
| **DeepSeek-R1-Distill-Qwen-7B** | <a href="https://cloud.siliconflow.cn" target="_blank" rel="noopener noreferrer">硅基流动 (SiliconFlow)</a> | 🟢 长期免费 | **无限量免费调用** (带 Free 标识，受并发限制) | 32K | ✅ 是 |
| **ERNIE-Speed-128K** | <a href="https://console.bce.baidu.com/qianfan" target="_blank" rel="noopener noreferrer">百度千帆平台</a> | 🟢 长期免费 | **官方全面永久免费**，超长 128K 上下文 | 128K | ✅ 是 |
| **DeepSeek-V3 / R1 (官方)** | <a href="https://platform.deepseek.com" target="_blank" rel="noopener noreferrer">DeepSeek 开放平台</a> | 🟠 新用户免费 | 注册赠送 **500 万 Tokens** (或 10 元代金券) | 64K | ✅ 是 |
| **Spark Lite** | <a href="https://xinghuo.xfyun.cn" target="_blank" rel="noopener noreferrer">讯飞开放平台</a> | 🟢 长期免费 | **永久免费开放**，轻量中文极速对话 | 8K | ✅ 是 |
| **Qwen-Plus / Qwen-Turbo** | <a href="https://bailian.console.aliyun.com" target="_blank" rel="noopener noreferrer">阿里云百炼 (DashScope)</a> | 🟡 有免费额度 | 开通赠送各模型 **100万~200万 Tokens** (90天) | 128K | ✅ 是 |

---

## 🚀 不知道选哪个？

根据你的真实开发场景，直接使用经过实测的最佳模型方案：

| 业务场景 | 首选推荐 | 备选推荐 | 选型依据与优势 |
| :--- | :--- | :--- | :--- |
| **🔥 当前最值得领取 (限时/高额福利)** | **Z.ai / ZCode** `GLM-5.3-Flash`<br>**移动云 墨玛** `DeepSeek-V4-Flash-0731` | **华为云 码道** `GLM5.3Flash`<br>**AMD 开发者** `DeepSeek V4 Flash` | ZCode 限时指定时段无限制免费刷 GLM-5.3-Flash；移动云开通免费赠送 2500 万 Tokens（爽玩 DeepSeek-V4 最新版）；华为云每天送 1000 万 Tokens。 |
| **💻 Coding / 代码编程与补全** | **魔搭** `Qwen2.5-Coder-32B-Instruct`<br>**移动云** `DeepSeek-V4-Flash-0731` | **ZCode** `GLM-5.3-Flash`<br>**华为云** `GLM5.3Flash` | Qwen2.5-Coder 专攻编程；移动云送 2500 万 Tokens 尽情调用 DeepSeek-V4 代码生成；ZCode 指定时段无限制。 |
| **⚡ Claude Code (替代后端)** | **智谱 AI** `glm-4-flash` | **魔搭** `deepseek-ai/DeepSeek-V3` | 原生中文高吞吐，支持标准 Function Call / Tool Calling 与长上下文，且永久免费。 |
| **🎯 Cursor / AI 编辑器** | **魔搭** `Qwen/Qwen2.5-Coder-32B-Instruct` | **硅基流动** `DeepSeek-R1-Distill-Qwen-7B` | 极简 OpenAI Compatible 地址配置，低延迟直连，不耗个人梯子流量。 |
| **⌨️ Codex CLI 终端助手** | **硅基流动** `Qwen/Qwen2.5-7B-Instruct` | **魔搭** `Qwen/Qwen2.5-72B-Instruct` | 毫秒级返回，终端执行命令与脚本编写体验丝滑。 |
| **🧠 Reasoning / 深度推理与算法** | **魔搭** `deepseek-ai/DeepSeek-R1` | **DeepSeek 官方** `deepseek-reasoner` | 具备顶尖思考链 (Chain of Thought) 推理能力，数学、算法与疑难 Debug 首选。 |
| **📜 长文本阅读与研报解析** | **百度千帆** `ernie-speed-128k` | **智谱 AI** `glm-4-flash` (128K) | 官方永久免费，128K 上下文支持整本小说、几十万字论文与财报全量抽取。 |
| **✍️ 中文写作、公文与通用** | **讯飞星火** `spark-lite`<br>**智谱 AI** `glm-4-flash` | **商汤日日新** `GLM / K3` | 讯飞与智谱中文语义理解精准且永久免费；商汤提供 60 万积分额度，通用中文问答极佳。 |
| **👁️ Vision / 图像理解与 OCR** | **魔搭** `Qwen/Qwen2.5-VL-72B-Instruct` | **火山引擎** `doubao-vision` (送额度) | 支持图表解析、界面截图转代码、复杂多模态 OCR 与视觉定位。 |

---

## 🔑 中国免费 API 快速入口

复制对应平台的 Base URL 与申请链接，1 分钟内完成接入：

| 平台 | 免费情况 | 获取 API Key 地址 | OpenAI Compatible Base URL | 备注说明 |
| :--- | :---: | :--- | :--- | :--- |
| **魔搭社区** | 🟢 长期免费 | <a href="https://modelscope.cn/my/myaccesstoken" target="_blank" rel="noopener noreferrer">获取 Access Token →</a> | `https://api-inference.modelscope.cn/v1/` | 每日 2000 次免费，涵盖数十款热门模型 |
| **智谱 AI** | 🟢 长期免费 | <a href="https://open.bigmodel.cn/usercenter/apikeys" target="_blank" rel="noopener noreferrer">创建 API Key →</a> | `https://open.bigmodel.cn/api/paas/v4` | GLM-4-Flash 永久免费，支持 128K |
| **硅基流动** | 🟢 长期免费 | <a href="https://cloud.siliconflow.cn/account/ak" target="_blank" rel="noopener noreferrer">创建 API Key →</a> | `https://api.siliconflow.cn/v1` | 免费模型子集无限量调用 |
| **百度千帆** | 🟢 长期免费 | <a href="https://console.bce.baidu.com/qianfan/overview" target="_blank" rel="noopener noreferrer">获取千帆 Key →</a> | `https://qianfan.baidubce.com/v2` | ERNIE-Speed/Lite 系列全面免费 |
| **讯飞星火** | 🟢 长期免费 | <a href="https://console.xfyun.cn/services/cbm" target="_blank" rel="noopener noreferrer">创建应用获取 Key →</a> | `https://spark-api-open.xf-yun.com/v1` | Spark Lite 永久免费 |
| **阿里云百炼** | 🟡 有免费额度 | <a href="https://bailian.console.aliyun.com/#/api-key" target="_blank" rel="noopener noreferrer">创建百炼 API-KEY →</a> | `https://dashscope.aliyuncs.com/compatible-mode/v1` | 通义千问各模型送 100万~200万 Tokens |
| **DeepSeek** | 🟠 新用户免费 | <a href="https://platform.deepseek.com/api_keys" target="_blank" rel="noopener noreferrer">创建 DeepSeek Key →</a> | `https://api.deepseek.com` | 注册送 500 万 Tokens (原厂 V3/R1) |
| **火山引擎** | 🟡 有免费额度 | <a href="https://console.volcengine.com/ark" target="_blank" rel="noopener noreferrer">创建火山 API Key →</a> | `https://ark.cn-beijing.volces.com/api/v3` | 每个模型接入点赠送 50万~500万 Tokens |
| **月之暗面 (Kimi)** | 🟠 新用户免费 | <a href="https://platform.moonshot.cn/console/api-keys" target="_blank" rel="noopener noreferrer">创建 Kimi Key →</a> | `https://api.moonshot.cn/v1` | 注册送 15 元体验额度 |
| **MiniMax** | 🟠 新用户免费 | <a href="https://platform.minimaxi.com/user-center/basic-information/interface-key" target="_blank" rel="noopener noreferrer">创建 MiniMax Key →</a> | `https://api.minimax.chat/v1` | 注册送 15 元额度，支持百万上下文 |
| **无问芯穹** | 🟢 长期免费 | <a href="https://cloud.infini-ai.com/api-key" target="_blank" rel="noopener noreferrer">获取 Infini Key →</a> | `https://cloud.infini-ai.com/maas/v1` | 每日赠送/免费调用 DeepSeek & Qwen |
| **零一万物** | 🟠 新用户免费 | <a href="https://platform.lingyiwanwu.com/apikeys" target="_blank" rel="noopener noreferrer">获取 01 Key →</a> | `https://api.lingyiwanwu.com/v1` | 注册赠送测试额度 (Yi-Lightning) |
| **Z.ai (智谱 GLM 计划)** | 🔥 限时免费 | <a href="https://z.ai" target="_blank" rel="noopener noreferrer">获取 Z.ai 权限 →</a> | `https://api.z.ai/v1` | 9.3~9.20 每天 23:00~09:00 在 ZCode 客户端完全无限制，第三方代理 2x 配额 |
| **移动云 (中国移动)** | 🟡 有免费额度 | <a href="https://ecloud.10086.cn/api/page/maas/moma/modelSquare" target="_blank" rel="noopener noreferrer">开通移动云 MaaS →</a> | 待控制台获取 | 开通体验赠送 2500 万 Tokens，支持 DeepSeek-V4-Flash-0731 |

---

## ⚡ OpenAI Compatible

本项目收录的所有平台均支持标准的 OpenAI 接口格式，只需设置 **Base URL**、**API Key** 和 **Model**：

```python
from openai import OpenAI

# 以智谱 AI (GLM-4-Flash 永久免费) 为例
client = OpenAI(
    api_key="YOUR_API_KEY",                          # 替换为你申请的 API Key
    base_url="https://open.bigmodel.cn/api/paas/v4"  # 替换为对应平台的 Base URL
)

response = client.chat.completions.create(
    model="glm-4-flash",                             # 替换为目标 Model ID
    messages=[
        {"role": "system", "content": "你是一位优秀的中文开发专家。"},
        {"role": "user", "content": "请用 Python 写一个支持超时重试的 HTTP 请求函数。"}
    ]
)

print(response.choices[0].message.content)
```

👉 **查看更多语言 (TypeScript, cURL, LangChain) 及厂商适配细节**：[OpenAI Compatible 详细指南](docs/openai-compatible.md)

---

## 💻 AI Coding 编程工具配置

中国免费 API 可直接无缝接入常用 AI 编程软件：

- **ZCode (智谱 Z.ai ADE)**：官方为 GLM 打造的桌面智能体编程开发环境，限时活动时段直连享受无限制 GLM-5.3-Flash。
- **Cursor**：`Settings` → `Models` → 勾选自定义 API Key，设置 Base URL（如 `https://api-inference.modelscope.cn/v1`）并添加模型 `Qwen/Qwen2.5-Coder-32B-Instruct`。
- **Claude Code**：配置本地中转代理（如 LiteLLM）或指定国内兼容端点，零门槛驱动 Agent 自动化编程。
- **Codex CLI**：`export OPENAI_BASE_URL="https://api.siliconflow.cn/v1"` 与 `export OPENAI_API_KEY="xxx"`，直接运行 `codex --model ...`。
- **Cline (VS Code)**：选择 `OpenAI Compatible` 模式，填入 Base URL 与 Key 即可。
- **OpenCode / Aider**：在配置文件中直接指定国内端点与模型。

👉 **查看各编程工具完整配置教程与模版**：[AI Coding 编程工具配置手册](docs/coding-tools.md)

---

## 📊 平台与模型详细档案

> 最后全量校验时间：**2026-09-07**

| 厂商 / 平台 | 模型名称 | 真实 Model ID | 免费状态 | 免费额度 / 规则 | 上下文 | 模态 | 实名认证 | 手机注册 | 充值门槛 |
| :--- | :--- | :--- | :---: | :--- | :---: | :---: | :---: | :---: | :---: |
| **魔搭社区** | Qwen2.5-72B | `Qwen/Qwen2.5-72B-Instruct` | 🟢 长期免费 | 每日 2000 次免费调用 (0点重置) | 128K | 文本/代码 | 否 | 是 | 无需充值 |
| **魔搭社区** | Qwen2.5-Coder-32B | `Qwen/Qwen2.5-Coder-32B-Instruct` | 🟢 长期免费 | 每日 2000 次免费调用 (0点重置) | 128K | 文本/代码 | 否 | 是 | 无需充值 |
| **魔搭社区** | DeepSeek-R1 | `deepseek-ai/DeepSeek-R1` | 🟢 长期免费 | 每日 2000 次免费调用 (0点重置) | 64K | 推理/文本 | 否 | 是 | 无需充值 |
| **魔搭社区** | DeepSeek-V3 | `deepseek-ai/DeepSeek-V3` | 🟢 长期免费 | 每日 2000 次免费调用 (0点重置) | 64K | 文本/代码 | 否 | 是 | 无需充值 |
| **魔搭社区** | Qwen2.5-VL-72B | `Qwen/Qwen2.5-VL-72B-Instruct` | 🟢 长期免费 | 每日 2000 次免费调用 (0点重置) | 32K | 图像/视觉 | 否 | 是 | 无需充值 |
| **硅基流动** | DeepSeek-R1-Distill-7B | `deepseek-ai/DeepSeek-R1-Distill-Qwen-7B` | 🟢 长期免费 | 免费子集无限量调用 (60 RPM) | 32K | 推理/文本 | 是 | 是 | 无需充值 |
| **硅基流动** | Qwen2.5-7B | `Qwen/Qwen2.5-7B-Instruct` | 🟢 长期免费 | 免费子集无限量调用 (60 RPM) | 32K | 文本/代码 | 是 | 是 | 无需充值 |
| **硅基流动** | GLM-4-9B-Chat | `THUDM/glm-4-9b-chat` | 🟢 长期免费 | 免费子集无限量调用 (60 RPM) | 32K | 文本 | 是 | 是 | 无需充值 |
| **智谱 AI** | GLM-4-Flash | `glm-4-flash` | 🟢 长期免费 | 永久免费商用，支持高并发 | 128K | 文本/代码 | 否 | 是 | 无需充值 |
| **百度千帆** | ERNIE-Speed-8K | `ernie-speed-8k` | 🟢 长期免费 | 官方永久免费开放 | 8K | 文本 | 是 | 是 | 无需充值 |
| **百度千帆** | ERNIE-Speed-128K | `ernie-speed-128k` | 🟢 长期免费 | 官方永久免费开放，超长上下文 | 128K | 文本 | 是 | 是 | 无需充值 |
| **百度千帆** | ERNIE-Lite-8K | `ernie-lite-8k` | 🟢 长期免费 | 官方永久免费开放 | 8K | 文本 | 是 | 是 | 无需充值 |
| **讯飞星火** | Spark Lite | `spark-lite` | 🟢 长期免费 | 永久免费，HTTP/WS 双接口 | 8K | 文本 | 是 | 是 | 无需充值 |
| **阿里云百炼** | Qwen-Plus | `qwen-plus` | 🟡 有免费额度 | 开通赠送 100 万 Tokens (90天) | 128K | 文本/代码 | 是 | 是 | 无需充值 |
| **阿里云百炼** | Qwen-Turbo | `qwen-turbo` | 🟡 有免费额度 | 开通赠送 200 万 Tokens (90天) | 128K | 文本/代码 | 是 | 是 | 无需充值 |
| **DeepSeek** | DeepSeek-V3 | `deepseek-chat` | 🟠 新用户免费 | 注册赠送 500 万 Tokens (1个月) | 64K | 文本/代码 | 否 | 是 | 无需充值 |
| **DeepSeek** | DeepSeek-R1 | `deepseek-reasoner` | 🟠 新用户免费 | 注册赠送 500 万 Tokens (1个月) | 64K | 推理/文本 | 否 | 是 | 无需充值 |
| **火山引擎** | Doubao-Lite-32k | `doubao-lite-32k` | 🟡 有免费额度 | 开通接入点赠送 500 万 Tokens | 32K | 文本 | 是 | 是 | 无需充值 |
| **Moonshot** | Moonshot-v1-8k | `moonshot-v1-8k` | 🟠 新用户免费 | 注册赠送 15 元额度包 | 8K | 文本 | 否 | 是 | 无需充值 |
| **MiniMax** | MiniMax-Text-01 | `MiniMax-Text-01` | 🟠 新用户免费 | 注册赠送 15 元额度，支持百万上下文 | 1M | 文本/代码 | 否 | 是 | 无需充值 |
| **商汤日日新 / 智子星** | GLM / K3 | `GLM / K3 (平台内)` | 🟡 有免费额度 | 约 60 万积分免费额度 (可使用 GLM、K3 等) | 平台内 | 文本/通用 | 否 | 是 | 无需充值 |
| **AMD 开发者** | DeepSeek V4 Flash | `DeepSeek V4 Flash` | 🔥 限时免费 | 当前完全免费使用 (限时福利，随时可能结束) | 平台内/待确认 | 文本/代码 | 否 | 是 | 无需充值 |
| **华为云 码道** | GLM5.3Flash | `GLM5.3Flash` | 🔥 限时免费 | 每人每天免费赠送 1000 万 Tokens | 平台内/待确认 | 文本/代码 | 是 | 是 | 无需充值 |
| **Z.ai / ZCode** | GLM-5.3-Flash | `glm-5.3-flash` | 🔥 限时免费 | 9.3~9.20 每天北京时间 23:00~09:00 在 ZCode 客户端内完全无限制免费；其他代理 2x 配额 | 128K | 文本/代码/视觉 | 否 | 否 | 无需充值 |
| **移动云 (中国移动)** | DeepSeek-V4-Flash-0731 | `DeepSeek-V4-Flash-0731` | 🟡 有免费额度 | 开通体验赠送 2500 万 Tokens 资源包 | 128K | 文本/代码 | 是 | 是 | 无需充值 |

---

## 📁 结构化数据 (JSON)

本项目所有厂商及模型数据均以结构化 JSON 保存在 [`data/`](data/) 目录中，便于程序调用、脚本集成或二次开发：

- [`data/providers.json`](data/providers.json)：厂商官网、API Key 申请地址、Base URL、认证要求等元数据。
- [`data/models.json`](data/models.json)：详细 Model ID、上下文大小、输入模态、限速 RPM/RPD、免费类型及验证记录。

---

## 🤝 贡献与反馈

欢迎提交 PR 补充或修正数据！提交时请确保：
1. 模型必须来自中国本土厂商或境内直连服务平台（不收录海外平台）。
2. 提供官方文档或官方公告的依据链接。
3. 标注准确的最后验证日期。

详细规范请参阅 [贡献指南 (CONTRIBUTING.md)](CONTRIBUTING.md)。

---

## 📄 开源许可证

本项目基于 [MIT License](LICENSE) 开源。
