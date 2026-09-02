# ⚡ OpenAI Compatible 接入指南

本项目收录的绝大多数中国大模型平台均支持 **OpenAI 兼容协议 (OpenAI Compatible API)**。这意味着你可以使用标准的 OpenAI SDK 或任何支持自定义 `base_url` 与 `api_key` 的工具无缝切换调用。

---

## 1. 核心通用配置清单

| 平台 | Base URL | 鉴权方式 (API Key) | 常用免费/主力 Model ID |
| :--- | :--- | :--- | :--- |
| **魔搭社区 (ModelScope)** | `https://api-inference.modelscope.cn/v1/` | Bearer Token (魔搭 Access Token) | `Qwen/Qwen2.5-72B-Instruct`<br>`Qwen/Qwen2.5-Coder-32B-Instruct`<br>`deepseek-ai/DeepSeek-R1` |
| **硅基流动 (SiliconFlow)** | `https://api.siliconflow.cn/v1` | Bearer API Key | `deepseek-ai/DeepSeek-R1-Distill-Qwen-7B`<br>`Qwen/Qwen2.5-7B-Instruct`<br>`THUDM/glm-4-9b-chat` |
| **智谱 AI (BigModel)** | `https://open.bigmodel.cn/api/paas/v4` | Bearer API Key | `glm-4-flash`<br>`glm-4.7-flash` |
| **百度千帆平台** | `https://qianfan.baidubce.com/v2` | Bearer API Key / Token | `ernie-speed-8k`<br>`ernie-speed-128k`<br>`ernie-lite-8k` |
| **讯飞星火** | `https://spark-api-open.xf-yun.com/v1` | Bearer API Key (APIPassword) | `spark-lite` |
| **阿里云百炼 (DashScope)** | `https://dashscope.aliyuncs.com/compatible-mode/v1` | Bearer API Key | `qwen-plus`<br>`qwen-turbo`<br>`qwen2.5-72b-instruct` |
| **DeepSeek (官方)** | `https://api.deepseek.com` | Bearer API Key | `deepseek-chat`<br>`deepseek-reasoner` |
| **火山引擎 (豆包/Ark)** | `https://ark.cn-beijing.volces.com/api/v3` | Bearer API Key | `doubao-lite-32k` / 自定义 Endpoint ID |
| **Moonshot (Kimi)** | `https://api.moonshot.cn/v1` | Bearer API Key | `moonshot-v1-8k`<br>`moonshot-v1-32k` |
| **MiniMax** | `https://api.minimax.chat/v1` | Bearer API Key | `MiniMax-Text-01` |
| **无问芯穹 (Infini-AI)** | `https://cloud.infini-ai.com/maas/v1` | Bearer API Key | `deepseek-r1`<br>`deepseek-v3` |

> ⚠️ **注意 Base URL 末尾路径**：
> - 智谱 AI 必须写 `/api/paas/v4`
> - 阿里云百炼必须写 `/compatible-mode/v1`
> - 百度千帆必须写 `/v2`
> - 魔搭社区必须写 `/v1/`

---

## 2. 常用开发语言调用示例

### 🐍 Python (OpenAI Official SDK)

先安装官方库：
```bash
pip install openai
```

#### 基础文本对话
```python
import os
from openai import OpenAI

# 以智谱 GLM-4-Flash 为例（永久免费）
client = OpenAI(
    api_key=os.environ.get("ZHIPU_API_KEY", "YOUR_API_KEY"),
    base_url="https://open.bigmodel.cn/api/paas/v4"
)

response = client.chat.completions.create(
    model="glm-4-flash",
    messages=[
        {"role": "system", "content": "你是一个资深的中文 AI 助手。"},
        {"role": "user", "content": "请用一句话介绍中国开源大模型的发展现状。"}
    ],
    temperature=0.7,
)

print(response.choices[0].message.content)
```

#### 流式输出 (Streaming)
```python
from openai import OpenAI

# 以硅基流动免费模型为例
client = OpenAI(
    api_key="YOUR_SILICONFLOW_API_KEY",
    base_url="https://api.siliconflow.cn/v1"
)

stream = client.chat.completions.create(
    model="deepseek-ai/DeepSeek-R1-Distill-Qwen-7B",
    messages=[{"role": "user", "content": "写一段 Python 快速排序算法"}],
    stream=True,
)

for chunk in stream:
    if chunk.choices and chunk.choices[0].delta.content:
        print(chunk.choices[0].delta.content, end="", flush=True)
print()
```

---

### 🌐 JavaScript / TypeScript (Node.js)

安装：
```bash
npm install openai
```

调用示例：
```javascript
import OpenAI from "openai";

// 以魔搭社区 Serverless 推理为例（每日 2000 次免费）
const openai = new OpenAI({
  apiKey: process.env.MODELSCOPE_API_KEY || "YOUR_MODELSCOPE_TOKEN",
  baseURL: "https://api-inference.modelscope.cn/v1/",
});

async function main() {
  const completion = await openai.chat.completions.create({
    messages: [{ role: "user", content: "你好！" }],
    model: "Qwen/Qwen2.5-72B-Instruct",
  });

  console.log(completion.choices[0].message.content);
}

main();
```

---

### 💻 cURL 命令行直接请求

```bash
# 智谱 GLM-4-Flash 调用
curl -X POST "https://open.bigmodel.cn/api/paas/v4/chat/completions" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer YOUR_API_KEY" \
     -d '{
       "model": "glm-4-flash",
       "messages": [
         {"role": "user", "content": "你好，请推荐 3 个中国优质开源项目"}
       ]
     }'
```

```bash
# 硅基流动免费 Qwen2.5-7B 调用
curl -X POST "https://api.siliconflow.cn/v1/chat/completions" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer YOUR_SILICONFLOW_API_KEY" \
     -d '{
       "model": "Qwen/Qwen2.5-7B-Instruct",
       "messages": [
         {"role": "user", "content": "Hello!"}
       ]
     }'
```

---

### 🦜️🔗 LangChain (Python)

```python
from langchain_openai import ChatOpenAI

llm = ChatOpenAI(
    model="Qwen/Qwen2.5-Coder-32B-Instruct",
    openai_api_key="YOUR_MODELSCOPE_TOKEN",
    openai_api_base="https://api-inference.modelscope.cn/v1/",
    temperature=0.2
)

response = llm.invoke("帮我写一个 Python 二分查找函数")
print(response.content)
```

---

## 3. 常见报错与排查 (Troubleshooting)

1. **401 Unauthorized / Invalid API Key**
   - 检查 API Key 是否复制完整，有无多余的前后空格或引号。
   - 检查请求头是否包含 `Bearer <API_KEY>`。

2. **404 Not Found**
   - 检查 Base URL 后缀是否正确。例如阿里云百炼缺少 `/compatible-mode/v1` 会返回 404，魔搭社区缺少 `/v1/` 会报错。

3. **429 Too Many Requests / Quota Exceeded**
   - 免费模型常有并发 (RPM) 限制。若触发 429，可适当增加重试或等待退避时间（Exponential Backoff）。
   - 魔搭社区若超过每日 2000 次限制，会在次日 00:00 (UTC+8) 自动恢复。
