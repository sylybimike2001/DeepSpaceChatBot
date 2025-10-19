# DeepSpaceChatBot
DeepSpaceChatBot
# 🌌 DeepSpaceChatBot — 深空探测任务助手

一个基于 **RAG（Retrieval-Augmented Generation）** 思想构建的混合式聊天机器人，结合了“知识检索 + 自然语言生成”两种能力。  
当用户提问与知识库高度相关的问题时，系统会返回精确答案；若知识库无法覆盖，则自动切换到生成模式，提供自然流畅的对话体验。

---

## 🧠 核心理念

在构建聊天机器人时，常见的两类方法：

| 方法 | 优点 | 缺点 |
|------|------|------|
| 🔍 **基于检索（Retrieval-based）** | 准确、可控，回答来源可靠 | 死板，覆盖面有限 |
| 💬 **基于生成（Generative-based）** | 灵活、自然，可处理开放式问题 | 不可控，可能产生“幻觉” |

➡️ **混合式（Hybrid）方法** 结合两者优点：  
优先使用检索来保证准确性，当检索无结果时再调用生成模型补充回答。

---

## 🚀 功能模块

- `retrieval_component.py`：使用 `sentence-transformers` 实现问答检索  
- `generative_component.py`：使用微软的 `DialoGPT` 实现自然语言生成  
- `main_chatbot.py`：整合逻辑，实现智能切换与完整对话流程  

---

## ⚙️ 环境依赖

```bash
pip install -r requirements.txt
