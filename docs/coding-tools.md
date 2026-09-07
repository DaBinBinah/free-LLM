# 💻 AI 编程工具免费 API 配置手册

本指南汇总了主流 AI 编程助手（Cursor、Claude Code、Codex CLI、Cline、OpenCode、Aider 等）接入中国免费大模型 API 的具体步骤与配置模板。

---

## 1. 🎯 Cursor 配置

Cursor 支持直接添加自定义 OpenAI 兼容模型。

### 配置步骤：
1. 打开 Cursor：点击右上角 **Settings** (设置) → **Models**。
2. 开启 **OpenAI API Key** 开关（或勾选使用自定义 API Key）。
3. 展开 **Override OpenAI Base URL**：
   - 若使用 **魔搭社区**：填入 `https://api-inference.modelscope.cn/v1`
   - 若使用 **硅基流动**：填入 `https://api.siliconflow.cn/v1`
   - 若使用 **智谱 AI**：填入 `https://open.bigmodel.cn/api/paas/v4`
   - 若使用 **DeepSeek**：填入 `https://api.deepseek.com`
4. 填入对应的 **API Key**。
5. 在 **Model Names** 列表中点击 **+ Add model**，填入真实 Model ID：
   - 编程推荐：`Qwen/Qwen2.5-Coder-32B-Instruct`
   - 推理推荐：`deepseek-ai/DeepSeek-R1-Distill-Qwen-7B` 或 `deepseek-chat`
   - 通用推荐：`glm-4-flash`
6. 保存并返回聊天窗口，在模型下拉菜单中选中刚才添加的模型即可！

---

## 2. ⚡ Claude Code 配置

Claude Code 官方默认连接 Anthropic 端点。连接国内兼容端点有以下两种主流方案：

### 方案 A：使用 Anthropic 兼容中转 / 环境变量直连
若使用支持 Anthropic 协议的代理或国内中转：
```bash
export ANTHROPIC_BASE_URL="https://your-anthropic-compatible-proxy/v1"
export ANTHROPIC_AUTH_TOKEN="your-api-key"
export ANTHROPIC_API_KEY="" # 保持为空以启用 AUTH_TOKEN
claude
```

### 方案 B：通过 LiteLLM 本地中转代理（推荐，100% 稳定）
1. 本地安装 LiteLLM：
   ```bash
   pip install litellm
   ```
2. 编写 `config.yaml`（以智谱 GLM-4-Flash 为例）：
   ```yaml
   model_list:
     - model_name: claude-3-5-sonnet-20241022
       litellm_params:
         model: openai/glm-4-flash
         api_base: https://open.bigmodel.cn/api/paas/v4
         api_key: os.environ/ZHIPU_API_KEY
   ```
3. 启动本地代理：
   ```bash
   litellm --config config.yaml --port 4000
   ```
4. 在终端启动 Claude Code：
   ```bash
   export ANTHROPIC_BASE_URL="http://localhost:4000"
   export ANTHROPIC_API_KEY="sk-litellm-any"
   claude
   ```

---

## 3. ⌨️ Codex CLI 配置

Codex CLI 默认完全遵循 OpenAI 环境变量标准：

```bash
# 1. 导出 API Base URL 与 Key（以魔搭社区为例）
export OPENAI_BASE_URL="https://api-inference.modelscope.cn/v1"
export OPENAI_API_KEY="YOUR_MODELSCOPE_TOKEN"

# 2. 指定模型启动 Codex
codex --model "Qwen/Qwen2.5-Coder-32B-Instruct"
```

如果使用硅基流动免费模型：
```bash
export OPENAI_BASE_URL="https://api.siliconflow.cn/v1"
export OPENAI_API_KEY="YOUR_SILICONFLOW_KEY"
codex --model "deepseek-ai/DeepSeek-R1-Distill-Qwen-7B"
```

---

## 4. 🧩 Cline (VS Code 插件)

1. 在 VS Code 中打开 Cline 扩展设置页面。
2. **API Provider** 下拉框选择：`OpenAI Compatible`。
3. **Base URL**：
   - 硅基流动：`https://api.siliconflow.cn/v1`
   - 魔搭社区：`https://api-inference.modelscope.cn/v1`
   - 智谱 AI：`https://open.bigmodel.cn/api/paas/v4`
4. **API Key**：填入你的 Key。
5. **Model ID**：
   - `Qwen/Qwen2.5-Coder-32B-Instruct`
   - `glm-4-flash`
   - `deepseek-chat`
6. 点击 **Done** 保存，即可在 Cline 中免费进行代码生成与项目级重构。

---

## 5. 🤖 OpenCode / OpenClaw

在项目或用户根目录的 `config.toml` 中配置：

```toml
[llm]
provider = "openai"
base_url = "https://open.bigmodel.cn/api/paas/v4"
api_key = "YOUR_ZHIPU_API_KEY"
model = "glm-4-flash"
temperature = 0.2
max_tokens = 4096
```

---

## 6. 🚀 Aider (终端结对编程)

在项目根目录下创建 `.aider.conf.yml` 或配置环境变量：

### 方式一：命令行参数
```bash
# 以硅基流动 DeepSeek R1 蒸馏版为例
export OPENAI_API_BASE="https://api.siliconflow.cn/v1"
export OPENAI_API_KEY="YOUR_SILICONFLOW_KEY"

aider --model openai/deepseek-ai/DeepSeek-R1-Distill-Qwen-7B
```

### 方式二：`.aider.conf.yml` 配置文件
```yaml
openai-api-base: https://api-inference.modelscope.cn/v1
openai-api-key: YOUR_MODELSCOPE_TOKEN
model: openai/Qwen/Qwen2.5-Coder-32B-Instruct
edit-format: diff
```

---

## 7. ⚡ ZCode / ZCodeX (智谱 ADE 官方代理开发环境) 与 GLM 编码计划

ZCode 是智谱 Z.ai 官方推出的 **Agentic Development Environment (ADE)** 桌面端智能体编程工作台，内置任务拆解规划、终端自动执行、代码库语义检索和浏览器自驱交互能力。

### 🌟 限时福利与时间规则 (2026.09.03 ~ 2026.09.20)
- **时段规则**：太平洋时间每天 **08:00 至 18:00**（对应 **北京时间每天 23:00 至次日 09:00**，极其适合夜间开发与跨夜自动化编程）。
- **客户端内福利**：在 ZCode 桌面客户端中，**完全无限制免费调用 GLM-5.3-Flash**（Unlimited）。
- **第三方代理福利**：在其他支持的编程代理（如 Claude Code、Cursor、Cline 等工具中配置 Z.ai Key）时，Flash 配额**直接享受 2x（双倍）加成**。

### 接入与使用指南：
1. **下载与安装 ZCode**：
   - 访问 <a href="https://z.ai" target="_blank" rel="noopener noreferrer">Z.ai 官网</a> 下载对应操作系统的 ZCode 客户端。
2. **账号登录与激活计划**：
   - 启动 ZCode，登录并进入“GLM 编码计划 (GLM Coding Plan)”专区。
3. **在 ZCode 中选择模型**：
   - 在工作区模型列表中选择 `GLM-5.3-Flash`，在北京时间每天 23:00 至次日 09:00 期间发起开发任务，自动享受无限制零额度扣除调用。
4. **在第三方编程代理（Cursor / Cline / Aider）中享受 2x 配额**：
   - 在 Z.ai 控制台创建 API Key。
   - **Base URL**：`https://api.z.ai/v1`
   - **Model ID**：`glm-5.3-flash`
   - 活动期间内通过外部代理调用可获得双倍额度。

---

## 💡 最佳使用建议与避坑提醒

1. **代码生成优先选择专用 Coder 模型**：`Qwen2.5-Coder-32B-Instruct` 在复杂逻辑与单测编写上表现非常出色。
2. **长文件重构优先选择大上下文模型**：例如智谱 `glm-4-flash` (128K) 或百度 `ernie-speed-128k` (128K)。
3. **遇到限流时做 Fallback 轮询**：建议同时申请 **智谱 AI (GLM-4-Flash)**、**魔搭社区 (Qwen2.5-72B)** 与 **硅基流动** 的免费 Key，互相备份，确保日常编程无缝不中断。
