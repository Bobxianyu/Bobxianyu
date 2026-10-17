# Hi, I'm Weitao Zhang 👋

## 关于我

🎓 软件工程本科生，就读于东莞理工学院。

💻 专注于 **AI 应用开发与后端工程方向**。

目前主要研究和实践：

- 🤖 LLM Application / Agent System
- 🧩 Multi-Agent 架构设计
- 🔍 RAG 知识检索系统
- ⚡ 后端服务与分布式系统
- 🦀 Rust 异步编程

我喜欢将大模型能力与可靠的软件工程结合，构建真正可落地的 AI 应用。


---

## 🚀 Featured Projects

### 🤖 ai-bid 智能标书合规审核系统

> Multi-Agent based intelligent bid compliance review system

一个基于 Multi-Agent 架构的智能标书合规审核平台，支持 PDF 文档解析、法规知识检索、多 Agent 协同审核以及结构化报告生成。

**技术栈：**

`Rust` `Tokio` `Axum` `ReAct` `LangChain4j` `Milvus` `SSE`

主要贡献：

-基于 Java + LangChain4j 独立完成法规知识 RAG 链路，实现 PDF 解析、文本切分、DashScope Embedding
与 Milvus 向量检索。
-面向现有 11 个审核 Agent 重构 Coordinator 执行控制，使用 Tokio JoinSet 与全局、文档两级 Semaphore
管理并行任务、分级超时、调用预算和失败回收；固定响应压测中，120 条款的存活模型客户端峰值
120→3，8 文档的在途调用峰值 24→12。
-将 SessionGraph 收敛为 RwLock<GraphState> ，结合 ReviewAttempt 生命周期和条款版本号支持并发增量
读取；在 5 万次本地基准中，完整读取耗时降低 71.86%、未变版本轮询耗时降低 98.81%，2.2 万次并发快
照检查的异常数 1,095→0。
-统一风险、引用与审计结果的状态流转及最终裁决，并处理重跑、超时、panic 和 SSE 取消时的资源回收；23
组故障场景、690 个独立进程验证通过。真实模型各三轮的前后版本对照中，新版 Confirmed 风险与最终结果
均全字段一致。


🔗 Repository:
https://github.com/dgut-hsd/ai-bid


---

### 🧠 LeapMind AI 互动教学平台

> Event-driven user profile engine for AI education platform

面向 AI 教育平台的用户画像计算引擎，通过分析学生学习行为，为学习诊断和个性化推荐提供数据支持。

**技术栈：**

`Python` `FastAPI` `Pydantic` `MySQL`

主要贡献：

- 设计事件驱动用户画像计算引擎，处理答题、练习、追问、反馈等学习行为事件。
- 实现知识点掌握度计算模型，包括事件权重和时间衰减机制。
- 开发学习趋势分析和知识点混淆识别能力。
- 完成多个模块接口联调及系统集成测试。


🔗 Repository:
https://github.com/dgut-hsd/leapmind


---

## 🛠️ 技术栈

### Languages

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat&logo=rust&logoColor=white)


### Backend Development

- Spring Boot
- FastAPI
- MyBatis-Plus
- RESTful API


### AI Engineering

- Large Language Model Application
- ReAct Agent
- Multi-Agent System
- RAG Architecture
- LangChain / LangChain4j
- Vector Database


### Database & Infrastructure

- MySQL
- Redis
- Milvus
- Docker
- Docker Compose
- Git


---

## 🏆 Achievements

🥉 2026 抖音 AI 创变者计划互动空间赛道

🏅 全国前 30

作品：
> 《逃声》—— 抖音互动空间音频交互小游戏


---

## 📚 Currently Learning

- Agent Architecture Design
- Rust Async Runtime
- Distributed System
- AI Engineering Best Practices


---

## 📫 Contact Me

GitHub:
https://github.com/Bobxianyu

Email:
your-email@example.com
