# 袁振洋 · Yuan Zhenyang 👋

哈尔滨工业大学（深圳）电子信息硕士研究生，方向：**Agent 开发 / LLM 应用工程 / Agent Runtime**。

从零实现过两个完整的 Agent 工程——一个用 LLM 自动做超参数寻优的实验 Harness，一个做中文论文调研与知识库的 RAG/Memory Agent，都配了 Eval 与可视化。

## 🚀 Agent 项目

### 1️⃣ Nonlinear NN Agent Harness — 超参数寻优实验 Agent

LLM 自动设计并执行非线性建模实验：plan → validate → execute → observe → reflect 闭环、可定制超参白名单、四种搜索策略公平对照、SQLite 控制面与 SSE 实时观测。

[🔗 GitHub](https://github.com/yzy-151/nonlinear-nn-agent) · Python · FastAPI · SQLite · Optuna · SSE

![Harness Web UI](https://raw.githubusercontent.com/yzy-151/nonlinear-nn-agent/main/docs/assets/screenshots/web-ui-home.png)

- 真实 LLM 闭环 10-case 命中率 **0.9**，最优 NMSE **-42.43 dB**
- 程序化 Reflection 稳定领先（paired delta **-4.28 dB**，95% CI 显著）
- SQLite 控制面：并发压测重复执行率 / 事件丢失率均为 **0**，故障恢复率 1.0
- **230+** 项自动化测试

### 2️⃣ PaperStorm — 中文论文调研与知识库 Agent

基于 Stanford STORM 二次开发：LangGraph 状态图编排、RAG 混合检索、跨会话 Memory、生产级 SQLite 治理控制面与调试 Dashboard。

[🔗 GitHub](https://github.com/yzy-151/paperstorm-agent) · LangGraph · RAG · Memory · Multi-Agent

![PaperStorm Dashboard](https://raw.githubusercontent.com/yzy-151/nonlinear-nn-agent/main/docs/assets/screenshots/paperstorm-dashboard-chat.png)

- 检索 Recall@K：0.3625 → **0.9875**（真实向量，**+172%**）
- Context 压缩节省 **66.11%**，恢复正确率 100%
- Memory 写入/召回契约 100%，泄漏 / 重复 0
- **191** 项全链路回归测试

## 🔬 研究背景

- 无线通信算法：FDD MIMO、无源互调（PIM）干扰抑制、波束赋形与链路建模（华为无线算法实习）
- 非线性系统建模（MPDPD）、NMSE / PSD 评估
- 通信信号处理 × 深度学习的工程落地

## 🛠️ 技术栈

- **Agent 工程**：Agentic Loop、Tool Calling / ToolSpec、Schema Guard、Eval Harness、Runtime 可靠性（retry / 幂等 / checkpoint / SSE）、RAG（BM25 + Dense + RRF + Rerank）、跨会话 Memory、Multi-Agent
- **语言 / 框架**：Python、asyncio、PyTorch、FastAPI、LangGraph、SQLite、Optuna、NumPy / SciPy、Git、unittest
- **网页端**：自研 Web UI / Dashboard（SSE 实时事件流、诊断可视化）

## 📫 联系

- 邮箱：yz11765@163.com
- GitHub：[yzy-151](https://github.com/yzy-151)
